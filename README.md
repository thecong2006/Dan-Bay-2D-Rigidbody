using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class spawn : MonoBehaviour
{
    public float speed;
    [SerializeField] Rigidbody2D _myBody;

    private void Awake()
    {
        _myBody = GetComponent<Rigidbody2D>();
    }
    void FixedUpdate()
    {
        _myBody.velocity = new Vector2(_myBody.velocity.x,speed);
    }
}

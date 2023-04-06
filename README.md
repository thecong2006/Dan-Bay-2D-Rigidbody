using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class spawn : MonoBehaviour
{
    public float speed; //Tốc độ
    [SerializeField] Rigidbody2D _myBody; //Biến Rigidbody

    private void Awake()
    {
        _myBody = GetComponent<Rigidbody2D>(); //Làm rõ để lấy Rigidbody của gameOb
    }
    void FixedUpdate()
    {
        _myBody.velocity = new Vector2(_myBody.velocity.x,speed);
    }
}

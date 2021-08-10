<template>
    <section class="activity">
        <h2 class="activity__title">Appointment Activity</h2>
        <div class="table">
            <div class="table__heading">
                <h4 class="table__heading-item first-item">Name</h4>
                <h4 class="table__heading-item second-item">Email</h4>
                <h4 class="table__heading-item">Date</h4>
                <h4 class="table__heading-item">Visit Time</h4>
                <h4 class="table__heading-item">Doctor</h4>
                <h4 class="table__heading-item">Conditions</h4>
            </div>
            <Table-content v-for="(item, index) in tables" :key="index" 
            :img="item.img"
            :user="item.user"
            :mail="item.mail"
            :date="item.date"
            :time="item.time"
            :doctor="item.doc"
            :condition="item.illness" />
            
        </div>
    </section>
</template>

<script>
import TableContent from './TableContent.vue'
export default {
  components: { TableContent },
    name: "Activity",
    data () {
        return {
            
            tables: [
                {
                    img: "https://picsum.photos/50/50",
                    user: "Leslie Alexander",
                    mail: "lesie.alexander@example.com",
                    date: "10/10/2020",
                    time: "09:15-09:45am",
                    doc: "Dr. Jacob Jones",
                    illness: "Mumps Stage II"
                },
                {
                    img: "https://picsum.photos/51/50",
                    user: "Ronald Richards",
                    mail: "ronald.richards@example.com",
                    date: "10/12/2020",
                    time: "12:00-12:45pm",
                    doc: "Dr. Theresa Webb",
                    illness: "Depression"
                },
                {
                    img: "https://picsum.photos/50/51",
                    user: "Jane Cooper",
                    mail: "jane.cooper@example.com",
                    date: "10/13/2020",
                    time: "01:15-01:45pm",
                    doc: "Dr. Jacob Jones",
                    illness: "Arthritis"
                },
                {
                    img: "https://picsum.photos/52/50",
                    user: "Robert Fox",
                    mail: "robert.fox@gmail.com",
                    date: "10/14/2020",
                    time: "02:00-02:45pm",
                    doc: "Dr. Arlene McCoy",
                    illness: "Fracture"
                },
                {
                    img: "https://picsum.photos/50/52",
                    user: "Jenny Wilson",
                    mail: "jenny.wilson@example.com",
                    date: "10/15/2020",
                    time: "12:00-12:45pm",
                    doc: "Dr. Esther Howard",
                    illness: " "
                }
                
            ]
        }
    },
    
}
</script>

<style lang="scss">
.d-none {
    display: none !important;
}
.activity {
    background: #FFFFFF;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    margin-top: 24px;
    &__title {
        font-weight: bold;
        font-size: 20px;
        line-height: 26px;
        color: #25282B;
        margin-bottom: 36px;
        padding: 24px;
    }
    .table {
        display: flex;
        flex-direction: column;
        &__heading {
            background: #E8E8E8;
            opacity: 0.2;
            display: flex;
            padding: 17px 24px;
            
            &-item {
                flex-basis: 14%;
                font-weight: bold;
                font-size: 14px;
                line-height: 20px;
                color: #25282B;
                text-align: left;
            }
            .first-item {
                flex-basis: 20%;
            }
            .second-item {
                flex-basis: 20%;
            }
        }
       
    }
    
}
</style>
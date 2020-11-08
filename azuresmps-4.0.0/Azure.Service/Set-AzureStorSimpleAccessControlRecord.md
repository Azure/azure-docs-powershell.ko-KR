---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045858"
---
# <span data-ttu-id="96393-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="96393-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="96393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96393-102">SYNOPSIS</span></span>
<span data-ttu-id="96393-103">액세스 제어 레코드의 IQN을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="96393-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96393-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96393-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96393-105">DESCRIPTION</span></span>
<span data-ttu-id="96393-106">**AzureStorSimpleAccessControlRecord** cmdlet은 기존 액세스 제어 레코드의 IQN (iSCSI 정규화 된 이름)을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="96393-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96393-107">EXAMPLES</span></span>

### <span data-ttu-id="96393-108">예제 1: 액세스 제어 레코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="96393-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="96393-109">이 명령은 IqnUpdated 이라는 iSCSI 초기자에 대 한 Acr10 라는 액세스 제어 레코드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="96393-110">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="96393-111">변수</span><span class="sxs-lookup"><span data-stu-id="96393-111">PARAMETERS</span></span>

### <span data-ttu-id="96393-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="96393-112">-ACRName</span></span>
<span data-ttu-id="96393-113">수정할 액세스 제어 레코드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-113">Specifies a name of the access control record to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96393-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="96393-114">-IQNInitiatorName</span></span>
<span data-ttu-id="96393-115">이 cmdlet이 볼륨에 대 한 액세스를 제공 하는 iSCSI 초기자의 IQN을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96393-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="96393-116">-NewName</span></span>
<span data-ttu-id="96393-117">액세스 제어 레코드의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96393-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="96393-118">-Profile</span></span>
<span data-ttu-id="96393-119">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-119">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96393-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="96393-120">-WaitForComplete</span></span>
<span data-ttu-id="96393-121">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="96393-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96393-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96393-122">CommonParameters</span></span>
<span data-ttu-id="96393-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96393-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96393-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96393-125">입력</span><span class="sxs-lookup"><span data-stu-id="96393-125">INPUTS</span></span>

### <span data-ttu-id="96393-126">않아야</span><span class="sxs-lookup"><span data-stu-id="96393-126">None</span></span>

## <span data-ttu-id="96393-127">출력</span><span class="sxs-lookup"><span data-stu-id="96393-127">OUTPUTS</span></span>

### <span data-ttu-id="96393-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="96393-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="96393-129">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="96393-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="96393-130">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96393-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="96393-131">상속자</span><span class="sxs-lookup"><span data-stu-id="96393-131">NOTES</span></span>

## <span data-ttu-id="96393-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96393-132">RELATED LINKS</span></span>

[<span data-ttu-id="96393-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="96393-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="96393-134">새로운 AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="96393-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="96393-135">제거-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="96393-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)



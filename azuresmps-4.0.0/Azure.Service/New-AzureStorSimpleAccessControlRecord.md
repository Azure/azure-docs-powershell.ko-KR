---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046210"
---
# <span data-ttu-id="b1131-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b1131-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="b1131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1131-102">SYNOPSIS</span></span>
<span data-ttu-id="b1131-103">액세스 제어 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-103">Creates an access control record.</span></span>

## <span data-ttu-id="b1131-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1131-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1131-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1131-105">DESCRIPTION</span></span>
<span data-ttu-id="b1131-106">**AzureStorSimpleAccessControlRecord** cmdlet은 액세스 제어 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="b1131-107">**Accesscontrolrecord** 개체를 사용 하 여 볼륨을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="b1131-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b1131-108">EXAMPLES</span></span>

### <span data-ttu-id="b1131-109">예제 1: Access control Access 컨트롤 레코드를 만들고 resultaccess 컨트롤을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="b1131-110">이 명령은 Iqn10 이라는 iSCSI 초기자에 대 한 Acr10 라는 액세스 제어 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="b1131-111">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="b1131-112">예제 2: Access 컨트롤 만들기 ' recordaccess 컨트롤에 대 한 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="b1131-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="b1131-113">이 명령은 Iqn11 이라는 iSCSI 초기자에 대 한 Acr11 라는 액세스 제어 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="b1131-114">이 명령은 *Waitforcomplete* 매개 변수를 지정 하지 않으므로 명령이 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b1131-115">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="b1131-116">변수</span><span class="sxs-lookup"><span data-stu-id="b1131-116">PARAMETERS</span></span>

### <span data-ttu-id="b1131-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="b1131-117">-ACRName</span></span>
<span data-ttu-id="b1131-118">액세스 제어 레코드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="b1131-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="b1131-119">-IQNInitiatorName</span></span>
<span data-ttu-id="b1131-120">이 cmdlet이 볼륨에 대 한 액세스를 제공 하는 iSCSI 초기자의 IQN (iSCSI 정규화 된 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="b1131-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="b1131-121">-Profile</span></span>
<span data-ttu-id="b1131-122">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b1131-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b1131-123">-WaitForComplete</span></span>
<span data-ttu-id="b1131-124">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b1131-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1131-125">CommonParameters</span></span>
<span data-ttu-id="b1131-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1131-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1131-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1131-128">입력</span><span class="sxs-lookup"><span data-stu-id="b1131-128">INPUTS</span></span>

### <span data-ttu-id="b1131-129">않아야</span><span class="sxs-lookup"><span data-stu-id="b1131-129">None</span></span>

## <span data-ttu-id="b1131-130">출력</span><span class="sxs-lookup"><span data-stu-id="b1131-130">OUTPUTS</span></span>

### <span data-ttu-id="b1131-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b1131-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="b1131-132">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b1131-133">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1131-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="b1131-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b1131-134">NOTES</span></span>

## <span data-ttu-id="b1131-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1131-135">RELATED LINKS</span></span>

[<span data-ttu-id="b1131-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b1131-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b1131-137">제거-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b1131-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b1131-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b1131-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b1131-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="b1131-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



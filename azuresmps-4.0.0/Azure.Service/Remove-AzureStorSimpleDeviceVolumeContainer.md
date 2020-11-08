---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046453"
---
# <span data-ttu-id="67240-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="67240-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="67240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67240-102">SYNOPSIS</span></span>
<span data-ttu-id="67240-103">StorSimple 장치에서 볼륨 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="67240-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67240-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67240-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67240-105">DESCRIPTION</span></span>
<span data-ttu-id="67240-106">**AzureStorSimpleDeviceVolumeContainer** Cmdlet은 StorSimple 장치에서 볼륨 컨테이너 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="67240-107">이 cmdlet은 *Force* 매개 변수를 지정 하지 않는 한 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="67240-108">예제의</span><span class="sxs-lookup"><span data-stu-id="67240-108">EXAMPLES</span></span>

### <span data-ttu-id="67240-109">예제 1: 파이프라인을 사용 하 여 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="67240-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="67240-110">이 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에서 Container08 이라는 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67240-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="67240-111">이 명령은 파이프라인 연산자를 사용 하 여 볼륨 컨테이너를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="67240-112">이 명령은 컨테이너를 제거 하는 작업을 시작 하 고 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="67240-113">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="67240-114">이 명령은 *Force* 매개 변수를 지정 하므로 확인을 묻는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67240-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="67240-115">변수</span><span class="sxs-lookup"><span data-stu-id="67240-115">PARAMETERS</span></span>

### <span data-ttu-id="67240-116">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="67240-116">-DeviceName</span></span>
<span data-ttu-id="67240-117">제거할 볼륨 컨테이너가 존재 하는 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67240-118">-Force</span><span class="sxs-lookup"><span data-stu-id="67240-118">-Force</span></span>
<span data-ttu-id="67240-119">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67240-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="67240-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="67240-120">-Profile</span></span>
<span data-ttu-id="67240-121">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="67240-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="67240-122">-VolumeContainer</span></span>
<span data-ttu-id="67240-123">제거할 볼륨 컨테이너를 **DataContainer** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="67240-124">**DataContainer** 개체를 얻으려면 **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67240-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="67240-125">-WaitForComplete</span></span>
<span data-ttu-id="67240-126">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67240-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="67240-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67240-127">CommonParameters</span></span>
<span data-ttu-id="67240-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67240-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67240-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67240-130">입력</span><span class="sxs-lookup"><span data-stu-id="67240-130">INPUTS</span></span>

### <span data-ttu-id="67240-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="67240-131">DataContainer</span></span>
<span data-ttu-id="67240-132">이 cmdlet은 **DataContainer** 개체를 허용 하 여 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="67240-133">출력</span><span class="sxs-lookup"><span data-stu-id="67240-133">OUTPUTS</span></span>

### <span data-ttu-id="67240-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="67240-134">TaskStatusInfo</span></span>
<span data-ttu-id="67240-135">*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67240-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="67240-136">상속자</span><span class="sxs-lookup"><span data-stu-id="67240-136">NOTES</span></span>

## <span data-ttu-id="67240-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67240-137">RELATED LINKS</span></span>

[<span data-ttu-id="67240-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="67240-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="67240-139">새로운 AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="67240-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)



---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046012"
---
# <span data-ttu-id="0ae05-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0ae05-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="0ae05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae05-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae05-103">StorSimple 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="0ae05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae05-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ae05-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae05-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae05-106">**AzureStorSimpleJob** cmdlet은 지속적인 StorSimple 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="0ae05-107">인스턴스 ID 또는 작업 이름을 제공 하 여 작업을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="0ae05-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae05-108">EXAMPLES</span></span>

### <span data-ttu-id="0ae05-109">예제 1: 장치에 대 한 작업 중지</span><span class="sxs-lookup"><span data-stu-id="0ae05-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="0ae05-110">이 명령은 Device07 이라는 장치에 대 한 작업을 **Get-AzureStorSimpleJob** cmdlet을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="0ae05-111">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 작업을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0ae05-112">현재 cmdlet은 명령이 전달 하는 모든 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="0ae05-113">명령에서 *Force* 매개 변수를 지정 하므로 작업을 중지 하기 전에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="0ae05-114">예제 2: 특정 작업 중지</span><span class="sxs-lookup"><span data-stu-id="0ae05-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="0ae05-115">이 명령은 지정 된 인스턴스 ID가 있는 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="0ae05-116">변수</span><span class="sxs-lookup"><span data-stu-id="0ae05-116">PARAMETERS</span></span>

### <span data-ttu-id="0ae05-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0ae05-117">-Force</span></span>
<span data-ttu-id="0ae05-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ae05-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0ae05-119">-InstanceId</span></span>
<span data-ttu-id="0ae05-120">중지할 장치 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae05-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="0ae05-121">-Profile</span></span>
<span data-ttu-id="0ae05-122">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0ae05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae05-123">CommonParameters</span></span>
<span data-ttu-id="0ae05-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae05-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae05-126">입력</span><span class="sxs-lookup"><span data-stu-id="0ae05-126">INPUTS</span></span>

### <span data-ttu-id="0ae05-127">않아야</span><span class="sxs-lookup"><span data-stu-id="0ae05-127">None</span></span>

## <span data-ttu-id="0ae05-128">출력</span><span class="sxs-lookup"><span data-stu-id="0ae05-128">OUTPUTS</span></span>

### <span data-ttu-id="0ae05-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="0ae05-129">DeviceJobDetails</span></span>
<span data-ttu-id="0ae05-130">이 cmdlet은이 cmdlet이 중지 하는 **Devicejob** 에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ae05-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="0ae05-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae05-131">NOTES</span></span>

## <span data-ttu-id="0ae05-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae05-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ae05-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0ae05-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



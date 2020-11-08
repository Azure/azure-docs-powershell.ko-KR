---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045650"
---
# <span data-ttu-id="59bca-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="59bca-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="59bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59bca-102">SYNOPSIS</span></span>
<span data-ttu-id="59bca-103">Azure가 가상 컴퓨터 및 클라우드 서비스에 영향을 주는 이벤트에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="59bca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59bca-104">SYNTAX</span></span>

### <span data-ttu-id="59bca-105">GetDeploymentEventBySlot (기본값)</span><span class="sxs-lookup"><span data-stu-id="59bca-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="59bca-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="59bca-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="59bca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59bca-107">DESCRIPTION</span></span>
<span data-ttu-id="59bca-108">**Get-AzureDeploymentEvent** Cmdlet은 Azure가 가상 컴퓨터 및 클라우드 서비스에 영향을 주는 이벤트에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="59bca-109">이러한 이벤트에는 계획 된 유지 관리 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="59bca-110">이 cmdlet은 역할 인스턴스 또는 가상 컴퓨터에 영향을 주는 이벤트 목록, 영향의 이유 및 이벤트 시작 시간을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="59bca-111">예제의</span><span class="sxs-lookup"><span data-stu-id="59bca-111">EXAMPLES</span></span>

### <span data-ttu-id="59bca-112">raid-1</span><span class="sxs-lookup"><span data-stu-id="59bca-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="59bca-113">변수</span><span class="sxs-lookup"><span data-stu-id="59bca-113">PARAMETERS</span></span>

### <span data-ttu-id="59bca-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="59bca-114">-DeploymentName</span></span>
<span data-ttu-id="59bca-115">이 cmdlet에서 이벤트를 가져오는 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="59bca-116">-EndTime</span></span>
<span data-ttu-id="59bca-117">이 cmdlet이 가져오는 예약 된 이벤트의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="59bca-118">-InformationAction</span></span>
<span data-ttu-id="59bca-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="59bca-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59bca-121">하기로</span><span class="sxs-lookup"><span data-stu-id="59bca-121">Continue</span></span>
- <span data-ttu-id="59bca-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="59bca-122">Ignore</span></span>
- <span data-ttu-id="59bca-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="59bca-123">Inquire</span></span>
- <span data-ttu-id="59bca-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="59bca-124">SilentlyContinue</span></span>
- <span data-ttu-id="59bca-125">중지가</span><span class="sxs-lookup"><span data-stu-id="59bca-125">Stop</span></span>
- <span data-ttu-id="59bca-126">대기</span><span class="sxs-lookup"><span data-stu-id="59bca-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="59bca-127">-InformationVariable</span></span>
<span data-ttu-id="59bca-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="59bca-129">-Profile</span></span>
<span data-ttu-id="59bca-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59bca-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59bca-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="59bca-132">-ServiceName</span></span>
<span data-ttu-id="59bca-133">이 cmdlet에서 예약 된 이벤트를 가져오는 호스팅된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="59bca-134">-Slot</span></span>
<span data-ttu-id="59bca-135">이 cmdlet에서 예약 된 이벤트를 가져오는 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="59bca-136">유효한 값은 스테이징 및 프로덕션입니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="59bca-137">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="59bca-138">-StartTime</span></span>
<span data-ttu-id="59bca-139">이 cmdlet이 가져오는 예약 된 이벤트의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bca-140">CommonParameters</span></span>
<span data-ttu-id="59bca-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bca-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bca-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bca-143">입력</span><span class="sxs-lookup"><span data-stu-id="59bca-143">INPUTS</span></span>

## <span data-ttu-id="59bca-144">출력</span><span class="sxs-lookup"><span data-stu-id="59bca-144">OUTPUTS</span></span>

## <span data-ttu-id="59bca-145">상속자</span><span class="sxs-lookup"><span data-stu-id="59bca-145">NOTES</span></span>

## <span data-ttu-id="59bca-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59bca-146">RELATED LINKS</span></span>

[<span data-ttu-id="59bca-147">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="59bca-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)



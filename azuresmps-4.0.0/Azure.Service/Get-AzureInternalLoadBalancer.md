---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046340"
---
# <span data-ttu-id="3089e-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3089e-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="3089e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3089e-102">SYNOPSIS</span></span>
<span data-ttu-id="3089e-103">내부 부하 분산 장치 구성에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="3089e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3089e-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3089e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3089e-105">DESCRIPTION</span></span>
<span data-ttu-id="3089e-106">**Get-AzureInternalLoadBalancer** Cmdlet은 Azure 서비스의 내부 부하 분산 장치 구성에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="3089e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3089e-107">EXAMPLES</span></span>

### <span data-ttu-id="3089e-108">예제 1: 내부 부하 분산 장치에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="3089e-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="3089e-109">이 명령은 **Get-help 서비스** cmdlet을 사용 하 여 ContosoService 라는 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="3089e-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 서비스를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3089e-111">현재 cmdlet은 해당 서비스의 내부 부하 분산 장치에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="3089e-112">변수</span><span class="sxs-lookup"><span data-stu-id="3089e-112">PARAMETERS</span></span>

### <span data-ttu-id="3089e-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3089e-113">-InformationAction</span></span>
<span data-ttu-id="3089e-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3089e-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3089e-116">하기로</span><span class="sxs-lookup"><span data-stu-id="3089e-116">Continue</span></span>
- <span data-ttu-id="3089e-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="3089e-117">Ignore</span></span>
- <span data-ttu-id="3089e-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="3089e-118">Inquire</span></span>
- <span data-ttu-id="3089e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3089e-119">SilentlyContinue</span></span>
- <span data-ttu-id="3089e-120">중지가</span><span class="sxs-lookup"><span data-stu-id="3089e-120">Stop</span></span>
- <span data-ttu-id="3089e-121">대기</span><span class="sxs-lookup"><span data-stu-id="3089e-121">Suspend</span></span>

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

### <span data-ttu-id="3089e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3089e-122">-InformationVariable</span></span>
<span data-ttu-id="3089e-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3089e-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="3089e-124">-Profile</span></span>
<span data-ttu-id="3089e-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3089e-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3089e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3089e-127">-ServiceName</span></span>
<span data-ttu-id="3089e-128">이 cmdlet이 내부 부하 분산 장치에 대 한 세부 정보를 가져오는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

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

### <span data-ttu-id="3089e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3089e-129">CommonParameters</span></span>
<span data-ttu-id="3089e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3089e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3089e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3089e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3089e-132">입력</span><span class="sxs-lookup"><span data-stu-id="3089e-132">INPUTS</span></span>

## <span data-ttu-id="3089e-133">출력</span><span class="sxs-lookup"><span data-stu-id="3089e-133">OUTPUTS</span></span>

### <span data-ttu-id="3089e-134">WindowsAzure. ServiceManagement. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="3089e-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="3089e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3089e-135">NOTES</span></span>

## <span data-ttu-id="3089e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3089e-136">RELATED LINKS</span></span>

[<span data-ttu-id="3089e-137">추가-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3089e-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="3089e-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="3089e-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="3089e-139">새로운 AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="3089e-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="3089e-140">제거-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3089e-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="3089e-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3089e-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)



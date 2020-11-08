---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046475"
---
# <span data-ttu-id="2ac07-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ac07-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="2ac07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac07-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac07-103">내부 부하 분산 장치 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="2ac07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ac07-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ac07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ac07-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac07-106">**제거-AzureInternalLoadBalancer** Cmdlet은 Azure 서비스에서 내부 부하 분산 장치 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="2ac07-107">끝점에서 현재 내부 부하 분산 장치를 참조 하는 경우에는이 cmdlet이 구성을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="2ac07-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2ac07-108">EXAMPLES</span></span>

### <span data-ttu-id="2ac07-109">예제 1: 내부 부하 분산 장치 구성 제거</span><span class="sxs-lookup"><span data-stu-id="2ac07-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="2ac07-110">이 명령은 ContosoService 이라는 서비스에 대 한 내부 부하 분산 장치 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="2ac07-111">변수</span><span class="sxs-lookup"><span data-stu-id="2ac07-111">PARAMETERS</span></span>

### <span data-ttu-id="2ac07-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ac07-112">-InformationAction</span></span>
<span data-ttu-id="2ac07-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ac07-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ac07-115">하기로</span><span class="sxs-lookup"><span data-stu-id="2ac07-115">Continue</span></span>
- <span data-ttu-id="2ac07-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="2ac07-116">Ignore</span></span>
- <span data-ttu-id="2ac07-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="2ac07-117">Inquire</span></span>
- <span data-ttu-id="2ac07-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ac07-118">SilentlyContinue</span></span>
- <span data-ttu-id="2ac07-119">중지가</span><span class="sxs-lookup"><span data-stu-id="2ac07-119">Stop</span></span>
- <span data-ttu-id="2ac07-120">대기</span><span class="sxs-lookup"><span data-stu-id="2ac07-120">Suspend</span></span>

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

### <span data-ttu-id="2ac07-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ac07-121">-InformationVariable</span></span>
<span data-ttu-id="2ac07-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ac07-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="2ac07-123">-Profile</span></span>
<span data-ttu-id="2ac07-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ac07-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ac07-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2ac07-126">-ServiceName</span></span>
<span data-ttu-id="2ac07-127">이 cmdlet이 내부 부하 분산을 제거 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="2ac07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac07-128">CommonParameters</span></span>
<span data-ttu-id="2ac07-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac07-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac07-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac07-131">입력</span><span class="sxs-lookup"><span data-stu-id="2ac07-131">INPUTS</span></span>

## <span data-ttu-id="2ac07-132">출력</span><span class="sxs-lookup"><span data-stu-id="2ac07-132">OUTPUTS</span></span>

### <span data-ttu-id="2ac07-133">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="2ac07-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="2ac07-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2ac07-134">NOTES</span></span>

## <span data-ttu-id="2ac07-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ac07-135">RELATED LINKS</span></span>

[<span data-ttu-id="2ac07-136">추가-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ac07-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="2ac07-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ac07-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="2ac07-138">새로운 AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="2ac07-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="2ac07-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ac07-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)



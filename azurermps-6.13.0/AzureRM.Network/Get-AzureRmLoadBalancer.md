---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530215"
---
# <span data-ttu-id="43f00-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43f00-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="43f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f00-102">SYNOPSIS</span></span>
<span data-ttu-id="43f00-103">부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43f00-104">SYNTAX</span></span>

### <span data-ttu-id="43f00-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="43f00-105">NoExpand (Default)</span></span>
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43f00-106">확장</span><span class="sxs-lookup"><span data-stu-id="43f00-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43f00-107">설명은</span><span class="sxs-lookup"><span data-stu-id="43f00-107">DESCRIPTION</span></span>
<span data-ttu-id="43f00-108">**AzureRmLoadBalancer** cmdlet은 리소스 그룹에 포함 된 하나 이상의 Azure 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="43f00-109">예제의</span><span class="sxs-lookup"><span data-stu-id="43f00-109">EXAMPLES</span></span>

### <span data-ttu-id="43f00-110">예제 1: 부하 분산 장치 가져오기</span><span class="sxs-lookup"><span data-stu-id="43f00-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="43f00-111">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="43f00-112">이 cmdlet을 실행 하려면 로드 균형 조정기가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="43f00-113">변수</span><span class="sxs-lookup"><span data-stu-id="43f00-113">PARAMETERS</span></span>

### <span data-ttu-id="43f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f00-114">-DefaultProfile</span></span>
<span data-ttu-id="43f00-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f00-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="43f00-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f00-117">-이름</span><span class="sxs-lookup"><span data-stu-id="43f00-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f00-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f00-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f00-119">CommonParameters</span></span>
<span data-ttu-id="43f00-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f00-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f00-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f00-122">입력</span><span class="sxs-lookup"><span data-stu-id="43f00-122">INPUTS</span></span>

### <span data-ttu-id="43f00-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43f00-123">System.String</span></span>

## <span data-ttu-id="43f00-124">출력</span><span class="sxs-lookup"><span data-stu-id="43f00-124">OUTPUTS</span></span>

### <span data-ttu-id="43f00-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43f00-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="43f00-126">상속자</span><span class="sxs-lookup"><span data-stu-id="43f00-126">NOTES</span></span>

## <span data-ttu-id="43f00-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43f00-127">RELATED LINKS</span></span>

[<span data-ttu-id="43f00-128">새로운 AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43f00-128">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="43f00-129">제거-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43f00-129">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="43f00-130">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43f00-130">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875583"
---
# <span data-ttu-id="45eb7-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45eb7-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="45eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="45eb7-103">부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-103">Gets a load balancer.</span></span>

## <span data-ttu-id="45eb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45eb7-104">SYNTAX</span></span>

### <span data-ttu-id="45eb7-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="45eb7-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45eb7-106">확장</span><span class="sxs-lookup"><span data-stu-id="45eb7-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45eb7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="45eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="45eb7-108">**AzLoadBalancer** cmdlet은 리소스 그룹에 포함 된 하나 이상의 Azure 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="45eb7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="45eb7-109">EXAMPLES</span></span>

### <span data-ttu-id="45eb7-110">예제 1: 부하 분산 장치 가져오기</span><span class="sxs-lookup"><span data-stu-id="45eb7-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="45eb7-111">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="45eb7-112">이 cmdlet을 실행 하려면 로드 균형 조정기가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="45eb7-113">변수</span><span class="sxs-lookup"><span data-stu-id="45eb7-113">PARAMETERS</span></span>

### <span data-ttu-id="45eb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45eb7-114">-DefaultProfile</span></span>
<span data-ttu-id="45eb7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45eb7-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="45eb7-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45eb7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="45eb7-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45eb7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45eb7-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45eb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45eb7-119">CommonParameters</span></span>
<span data-ttu-id="45eb7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45eb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45eb7-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45eb7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45eb7-122">입력</span><span class="sxs-lookup"><span data-stu-id="45eb7-122">INPUTS</span></span>

## <span data-ttu-id="45eb7-123">출력</span><span class="sxs-lookup"><span data-stu-id="45eb7-123">OUTPUTS</span></span>

### <span data-ttu-id="45eb7-124">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45eb7-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45eb7-125">상속자</span><span class="sxs-lookup"><span data-stu-id="45eb7-125">NOTES</span></span>

## <span data-ttu-id="45eb7-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45eb7-126">RELATED LINKS</span></span>

[<span data-ttu-id="45eb7-127">새로운 AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45eb7-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="45eb7-128">제거-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45eb7-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="45eb7-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45eb7-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)



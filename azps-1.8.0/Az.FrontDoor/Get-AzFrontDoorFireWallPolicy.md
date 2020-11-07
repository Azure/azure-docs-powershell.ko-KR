---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: e8fe8fb59ee56e457c49d959c07db08cad62bb5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868421"
---
# <span data-ttu-id="703a7-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="703a7-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="703a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="703a7-102">SYNOPSIS</span></span>
<span data-ttu-id="703a7-103">WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="703a7-103">Get WAF policy</span></span>

## <span data-ttu-id="703a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="703a7-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="703a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="703a7-105">DESCRIPTION</span></span>
<span data-ttu-id="703a7-106">**AzFrontDoorFireWallPolicy** cmdletget은 현재 구독 아래의 리소스 그룹에서 waf 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="703a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="703a7-107">EXAMPLES</span></span>

### <span data-ttu-id="703a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="703a7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="703a7-109">$resourceGroupName에 $policyName 이라는 WAF 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="703a7-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="703a7-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="703a7-111">$resourceGroupName에서 모든 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="703a7-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="703a7-112">변수</span><span class="sxs-lookup"><span data-stu-id="703a7-112">PARAMETERS</span></span>

### <span data-ttu-id="703a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703a7-113">-DefaultProfile</span></span>
<span data-ttu-id="703a7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703a7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="703a7-115">-Name</span></span>
<span data-ttu-id="703a7-116">FireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="703a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="703a7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="703a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703a7-119">CommonParameters</span></span>
<span data-ttu-id="703a7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="703a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703a7-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="703a7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703a7-122">입력</span><span class="sxs-lookup"><span data-stu-id="703a7-122">INPUTS</span></span>

### <span data-ttu-id="703a7-123">않아야</span><span class="sxs-lookup"><span data-stu-id="703a7-123">None</span></span>

## <span data-ttu-id="703a7-124">출력</span><span class="sxs-lookup"><span data-stu-id="703a7-124">OUTPUTS</span></span>

### <span data-ttu-id="703a7-125">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="703a7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="703a7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="703a7-126">NOTES</span></span>

## <span data-ttu-id="703a7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="703a7-127">RELATED LINKS</span></span>

<span data-ttu-id="703a7-128">[새로운 AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [제거-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="703a7-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span></span>

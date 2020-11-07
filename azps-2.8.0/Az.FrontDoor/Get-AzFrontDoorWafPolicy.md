---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 60d6263d3fb074cf4795379ae28f1824dc81a4c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689893"
---
# <span data-ttu-id="f5a8d-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a8d-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="f5a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a8d-103">WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f5a8d-103">Get WAF policy</span></span>

## <span data-ttu-id="f5a8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5a8d-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a8d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a8d-106">**AzFrontDoorWafPolicy** cmdletget은 현재 구독 아래의 리소스 그룹에서 waf 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="f5a8d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a8d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5a8d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="f5a8d-109">$resourceGroupName에 $policyName 이라는 WAF 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="f5a8d-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5a8d-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="f5a8d-111">$resourceGroupName에서 모든 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f5a8d-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="f5a8d-112">변수</span><span class="sxs-lookup"><span data-stu-id="f5a8d-112">PARAMETERS</span></span>

### <span data-ttu-id="f5a8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a8d-113">-DefaultProfile</span></span>
<span data-ttu-id="f5a8d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a8d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f5a8d-115">-Name</span></span>
<span data-ttu-id="f5a8d-116">FireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="f5a8d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a8d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5a8d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-118">The resource group name.</span></span>

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

### <span data-ttu-id="f5a8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a8d-119">CommonParameters</span></span>
<span data-ttu-id="f5a8d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a8d-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a8d-122">입력</span><span class="sxs-lookup"><span data-stu-id="f5a8d-122">INPUTS</span></span>

### <span data-ttu-id="f5a8d-123">않아야</span><span class="sxs-lookup"><span data-stu-id="f5a8d-123">None</span></span>

## <span data-ttu-id="f5a8d-124">출력</span><span class="sxs-lookup"><span data-stu-id="f5a8d-124">OUTPUTS</span></span>

### <span data-ttu-id="f5a8d-125">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f5a8d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f5a8d-126">NOTES</span></span>

## <span data-ttu-id="f5a8d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5a8d-127">RELATED LINKS</span></span>

<span data-ttu-id="f5a8d-128">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [제거-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f5a8d-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>

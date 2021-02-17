---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209509"
---
# <span data-ttu-id="82539-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="82539-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="82539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82539-102">SYNOPSIS</span></span>
<span data-ttu-id="82539-103">WAF 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="82539-103">Get WAF policy</span></span>

## <span data-ttu-id="82539-104">구문</span><span class="sxs-lookup"><span data-stu-id="82539-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82539-105">설명</span><span class="sxs-lookup"><span data-stu-id="82539-105">DESCRIPTION</span></span>
<span data-ttu-id="82539-106">**Get-AzFrontDoorWafPolicy** cmdletGet은 현재 구독의 리소스 그룹에서 WAF 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82539-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="82539-107">예제</span><span class="sxs-lookup"><span data-stu-id="82539-107">EXAMPLES</span></span>

### <span data-ttu-id="82539-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="82539-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="82539-109">다음에서 $policyName WAF 정책을 $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82539-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="82539-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="82539-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="82539-111">다음의 모든 WAF 정책을 $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82539-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="82539-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82539-112">PARAMETERS</span></span>

### <span data-ttu-id="82539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82539-113">-DefaultProfile</span></span>
<span data-ttu-id="82539-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82539-115">-Name</span><span class="sxs-lookup"><span data-stu-id="82539-115">-Name</span></span>
<span data-ttu-id="82539-116">FireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82539-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="82539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82539-117">-ResourceGroupName</span></span>
<span data-ttu-id="82539-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82539-118">The resource group name.</span></span>

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

### <span data-ttu-id="82539-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82539-119">CommonParameters</span></span>
<span data-ttu-id="82539-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82539-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82539-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82539-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82539-122">입력</span><span class="sxs-lookup"><span data-stu-id="82539-122">INPUTS</span></span>

### <span data-ttu-id="82539-123">없음</span><span class="sxs-lookup"><span data-stu-id="82539-123">None</span></span>

## <span data-ttu-id="82539-124">출력</span><span class="sxs-lookup"><span data-stu-id="82539-124">OUTPUTS</span></span>

### <span data-ttu-id="82539-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="82539-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="82539-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82539-126">NOTES</span></span>

## <span data-ttu-id="82539-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82539-127">RELATED LINKS</span></span>

<span data-ttu-id="82539-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="82539-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>

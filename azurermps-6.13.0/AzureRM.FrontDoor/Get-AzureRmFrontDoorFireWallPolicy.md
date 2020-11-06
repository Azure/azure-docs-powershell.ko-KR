---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531993"
---
# <span data-ttu-id="f246d-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="f246d-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="f246d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f246d-102">SYNOPSIS</span></span>
<span data-ttu-id="f246d-103">WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f246d-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f246d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f246d-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f246d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f246d-105">DESCRIPTION</span></span>
<span data-ttu-id="f246d-106">**AzureRmFrontDoorFireWallPolicy** cmdletget은 현재 구독 아래의 리소스 그룹에서 waf 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="f246d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f246d-107">EXAMPLES</span></span>

### <span data-ttu-id="f246d-108">예제 1: $resourceGroup에 $Name 이라는 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f246d-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="f246d-109">$resourceGroup에 $Name 이라는 WAF 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="f246d-110">예제 2: $resourceGroup에서 모든 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f246d-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="f246d-111">$resourceGroup에서 모든 WAF 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f246d-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="f246d-112">변수</span><span class="sxs-lookup"><span data-stu-id="f246d-112">PARAMETERS</span></span>

### <span data-ttu-id="f246d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f246d-113">-DefaultProfile</span></span>
<span data-ttu-id="f246d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f246d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f246d-115">-Name</span></span>
<span data-ttu-id="f246d-116">FireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="f246d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f246d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f246d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-118">The resource group name.</span></span>

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

### <span data-ttu-id="f246d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f246d-119">CommonParameters</span></span>
<span data-ttu-id="f246d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f246d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f246d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f246d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f246d-122">입력</span><span class="sxs-lookup"><span data-stu-id="f246d-122">INPUTS</span></span>

### <span data-ttu-id="f246d-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f246d-123">System.String</span></span>

## <span data-ttu-id="f246d-124">출력</span><span class="sxs-lookup"><span data-stu-id="f246d-124">OUTPUTS</span></span>

### <span data-ttu-id="f246d-125">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="f246d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f246d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f246d-126">NOTES</span></span>

## <span data-ttu-id="f246d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f246d-127">RELATED LINKS</span></span>

<span data-ttu-id="f246d-128">[새로운 AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [제거-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f246d-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>

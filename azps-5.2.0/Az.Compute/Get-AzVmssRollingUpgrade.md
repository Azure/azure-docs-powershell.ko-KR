---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335385"
---
# <span data-ttu-id="c526b-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c526b-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="c526b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c526b-102">SYNOPSIS</span></span>
<span data-ttu-id="c526b-103">최신 가상 머신 확장 집합 롤링 업그레이드의 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c526b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c526b-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c526b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c526b-105">DESCRIPTION</span></span>
<span data-ttu-id="c526b-106">최신 가상 머신 확장 집합 롤링 업그레이드의 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c526b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c526b-107">EXAMPLES</span></span>

### <span data-ttu-id="c526b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c526b-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c526b-109">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS의 최신 롤링 업그레이드 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c526b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c526b-110">PARAMETERS</span></span>

### <span data-ttu-id="c526b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c526b-111">-DefaultProfile</span></span>
<span data-ttu-id="c526b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c526b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c526b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c526b-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c526b-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c526b-115">-VMScaleSetName</span></span>
<span data-ttu-id="c526b-116">VM 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c526b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c526b-117">CommonParameters</span></span>
<span data-ttu-id="c526b-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c526b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c526b-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c526b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c526b-120">입력</span><span class="sxs-lookup"><span data-stu-id="c526b-120">INPUTS</span></span>

### <span data-ttu-id="c526b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c526b-121">System.String</span></span>

## <span data-ttu-id="c526b-122">출력</span><span class="sxs-lookup"><span data-stu-id="c526b-122">OUTPUTS</span></span>

### <span data-ttu-id="c526b-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="c526b-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="c526b-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c526b-124">NOTES</span></span>

## <span data-ttu-id="c526b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c526b-125">RELATED LINKS</span></span>

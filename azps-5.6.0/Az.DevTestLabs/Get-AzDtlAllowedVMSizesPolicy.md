---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: f1b5d95397aad24b84462c7e9ceba4a06ba854c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994359"
---
# <span data-ttu-id="6459c-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="6459c-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="6459c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6459c-102">SYNOPSIS</span></span>
<span data-ttu-id="6459c-103">DevTest Labs에서 랩의 허용된 가상 머신 크기 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="6459c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6459c-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6459c-105">설명</span><span class="sxs-lookup"><span data-stu-id="6459c-105">DESCRIPTION</span></span>
<span data-ttu-id="6459c-106">**Get-AzDtlAllowedVMSizesPolicy** cmdlet은 허용되는 가상 머신 크기 정책을 얻게 하여 랩에서 허용되는 가상 머신 크기 목록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="6459c-107">cmdlet은 정책의 사용 또는 사용 안 하도록 설정된 상태 및 지정된 정책에서 설정한 허용된 모든 가상 머신 크기 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="6459c-108">예제</span><span class="sxs-lookup"><span data-stu-id="6459c-108">EXAMPLES</span></span>

## <span data-ttu-id="6459c-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6459c-109">PARAMETERS</span></span>

### <span data-ttu-id="6459c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6459c-110">-DefaultProfile</span></span>
<span data-ttu-id="6459c-111">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6459c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6459c-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="6459c-112">-LabName</span></span>
<span data-ttu-id="6459c-113">이 cmdlet에서 가상 머신 크기 정책을 얻을 랩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="6459c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6459c-114">-ResourceGroupName</span></span>
<span data-ttu-id="6459c-115">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6459c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6459c-116">CommonParameters</span></span>
<span data-ttu-id="6459c-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6459c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6459c-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6459c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6459c-119">입력</span><span class="sxs-lookup"><span data-stu-id="6459c-119">INPUTS</span></span>

### <span data-ttu-id="6459c-120">System.String</span><span class="sxs-lookup"><span data-stu-id="6459c-120">System.String</span></span>

## <span data-ttu-id="6459c-121">출력</span><span class="sxs-lookup"><span data-stu-id="6459c-121">OUTPUTS</span></span>

### <span data-ttu-id="6459c-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6459c-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="6459c-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6459c-123">NOTES</span></span>

## <span data-ttu-id="6459c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6459c-124">RELATED LINKS</span></span>

[<span data-ttu-id="6459c-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="6459c-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)



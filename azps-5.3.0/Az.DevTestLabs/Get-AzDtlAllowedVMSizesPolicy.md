---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492035"
---
# <span data-ttu-id="b6420-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b6420-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="b6420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6420-102">SYNOPSIS</span></span>
<span data-ttu-id="b6420-103">DevTest Labs에서 랩의 허용되는 가상 머신 크기 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b6420-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6420-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6420-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6420-105">DESCRIPTION</span></span>
<span data-ttu-id="b6420-106">**Get-AzDtlAllowedVMSizesPolicy** cmdlet은 허용되는 가상 머신 크기 정책을 사용하여 랩에 허용되는 가상 머신 크기 목록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="b6420-107">cmdlet은 정책의 사용 또는 비활성화 상태와 지정된 정책에서 설정한 허용된 모든 가상 머신 크기 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="b6420-108">예제</span><span class="sxs-lookup"><span data-stu-id="b6420-108">EXAMPLES</span></span>

## <span data-ttu-id="b6420-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6420-109">PARAMETERS</span></span>

### <span data-ttu-id="b6420-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6420-110">-DefaultProfile</span></span>
<span data-ttu-id="b6420-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6420-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6420-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b6420-112">-LabName</span></span>
<span data-ttu-id="b6420-113">이 cmdlet이 가상 머신 크기 정책을 받을 랩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="b6420-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6420-114">-ResourceGroupName</span></span>
<span data-ttu-id="b6420-115">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b6420-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6420-116">CommonParameters</span></span>
<span data-ttu-id="b6420-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6420-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6420-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6420-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6420-119">입력</span><span class="sxs-lookup"><span data-stu-id="b6420-119">INPUTS</span></span>

### <span data-ttu-id="b6420-120">System.String</span><span class="sxs-lookup"><span data-stu-id="b6420-120">System.String</span></span>

## <span data-ttu-id="b6420-121">출력</span><span class="sxs-lookup"><span data-stu-id="b6420-121">OUTPUTS</span></span>

### <span data-ttu-id="b6420-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b6420-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b6420-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6420-123">NOTES</span></span>

## <span data-ttu-id="b6420-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6420-124">RELATED LINKS</span></span>

[<span data-ttu-id="b6420-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b6420-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)



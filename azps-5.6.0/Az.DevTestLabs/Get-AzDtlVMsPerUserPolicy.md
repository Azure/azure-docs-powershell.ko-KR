---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 7c2a7ef4c134d811d8c30266305f25d3d53b1289
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004203"
---
# <span data-ttu-id="5a42a-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5a42a-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="5a42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a42a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a42a-103">DevTest Labs에서 랩의 사용자당 가상 머신 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5a42a-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a42a-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a42a-105">설명</span><span class="sxs-lookup"><span data-stu-id="5a42a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a42a-106">**Get-AzDtlVMsPerUserPolicy** cmdlet은 랩의 사용자 정책당 가상 머신을 얻게 하여 사용자당 허용되는 최대 가상 머신 수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="5a42a-107">cmdlet은 정책의 사용 또는 사용 안 하도록 설정된 상태 및 정책에서 설정한 사용자당 허용되는 최대 가상 머신 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="5a42a-108">예제</span><span class="sxs-lookup"><span data-stu-id="5a42a-108">EXAMPLES</span></span>

## <span data-ttu-id="5a42a-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a42a-109">PARAMETERS</span></span>

### <span data-ttu-id="5a42a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a42a-110">-DefaultProfile</span></span>
<span data-ttu-id="5a42a-111">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a42a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a42a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="5a42a-112">-LabName</span></span>
<span data-ttu-id="5a42a-113">이 cmdlet에서 사용자 정책당 가상 머신을 얻을 랩 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="5a42a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a42a-114">-ResourceGroupName</span></span>
<span data-ttu-id="5a42a-115">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5a42a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a42a-116">CommonParameters</span></span>
<span data-ttu-id="5a42a-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a42a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a42a-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5a42a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a42a-119">입력</span><span class="sxs-lookup"><span data-stu-id="5a42a-119">INPUTS</span></span>

### <span data-ttu-id="5a42a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="5a42a-120">System.String</span></span>

## <span data-ttu-id="5a42a-121">출력</span><span class="sxs-lookup"><span data-stu-id="5a42a-121">OUTPUTS</span></span>

### <span data-ttu-id="5a42a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5a42a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="5a42a-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a42a-123">NOTES</span></span>

## <span data-ttu-id="5a42a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a42a-124">RELATED LINKS</span></span>

[<span data-ttu-id="5a42a-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5a42a-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)



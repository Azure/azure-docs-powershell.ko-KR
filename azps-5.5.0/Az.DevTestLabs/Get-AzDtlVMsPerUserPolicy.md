---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200436"
---
# <span data-ttu-id="0c9f0-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0c9f0-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0c9f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9f0-103">DevTest Labs에서 랩의 사용자 정책당 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="0c9f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c9f0-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9f0-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c9f0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9f0-106">**Get-AzDtlVMsPerUserPolicy** cmdlet은 랩의 사용자 정책당 가상 머신을 얻게 하여 사용자당 허용되는 최대 가상 머신 수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0c9f0-107">cmdlet은 정책의 사용 또는 비활성화 상태와 정책에서 설정한 사용자당 허용되는 최대 가상 머신 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="0c9f0-108">예제</span><span class="sxs-lookup"><span data-stu-id="0c9f0-108">EXAMPLES</span></span>

## <span data-ttu-id="0c9f0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c9f0-109">PARAMETERS</span></span>

### <span data-ttu-id="0c9f0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9f0-110">-DefaultProfile</span></span>
<span data-ttu-id="0c9f0-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c9f0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c9f0-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="0c9f0-112">-LabName</span></span>
<span data-ttu-id="0c9f0-113">이 cmdlet이 사용자 정책당 가상 머신을 얻을 랩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="0c9f0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9f0-114">-ResourceGroupName</span></span>
<span data-ttu-id="0c9f0-115">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0c9f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9f0-116">CommonParameters</span></span>
<span data-ttu-id="0c9f0-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9f0-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c9f0-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9f0-119">입력</span><span class="sxs-lookup"><span data-stu-id="0c9f0-119">INPUTS</span></span>

### <span data-ttu-id="0c9f0-120">System.String</span><span class="sxs-lookup"><span data-stu-id="0c9f0-120">System.String</span></span>

## <span data-ttu-id="0c9f0-121">출력</span><span class="sxs-lookup"><span data-stu-id="0c9f0-121">OUTPUTS</span></span>

### <span data-ttu-id="0c9f0-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0c9f0-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="0c9f0-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c9f0-123">NOTES</span></span>

## <span data-ttu-id="0c9f0-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c9f0-124">RELATED LINKS</span></span>

[<span data-ttu-id="0c9f0-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0c9f0-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)



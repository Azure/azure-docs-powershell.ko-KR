---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: fa19f45527302c858593d200fb2a6ed605d02321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974939"
---
# <span data-ttu-id="797fa-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="797fa-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="797fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797fa-102">SYNOPSIS</span></span>
<span data-ttu-id="797fa-103">DevTest Labs에서 랩의 랩당 가상 머신 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="797fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="797fa-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="797fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="797fa-105">DESCRIPTION</span></span>
<span data-ttu-id="797fa-106">**Get-AzDtlVMsPerLabPolicy** cmdlet은 랩의 랩 정책당 가상 머신을 얻게 하여 랩에서 허용되는 총 가상 머신 수를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="797fa-107">cmdlet은 정책의 사용 또는 사용 안 하도록 설정된 상태 및 정책에서 설정한 랩에서 허용되는 총 가상 머신 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="797fa-108">예제</span><span class="sxs-lookup"><span data-stu-id="797fa-108">EXAMPLES</span></span>

## <span data-ttu-id="797fa-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="797fa-109">PARAMETERS</span></span>

### <span data-ttu-id="797fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797fa-110">-DefaultProfile</span></span>
<span data-ttu-id="797fa-111">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="797fa-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="797fa-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="797fa-112">-LabName</span></span>
<span data-ttu-id="797fa-113">이 cmdlet에서 가상 머신을 얻을 랩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="797fa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797fa-114">-ResourceGroupName</span></span>
<span data-ttu-id="797fa-115">랩이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="797fa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797fa-116">CommonParameters</span></span>
<span data-ttu-id="797fa-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="797fa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797fa-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="797fa-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797fa-119">입력</span><span class="sxs-lookup"><span data-stu-id="797fa-119">INPUTS</span></span>

### <span data-ttu-id="797fa-120">System.String</span><span class="sxs-lookup"><span data-stu-id="797fa-120">System.String</span></span>

## <span data-ttu-id="797fa-121">출력</span><span class="sxs-lookup"><span data-stu-id="797fa-121">OUTPUTS</span></span>

### <span data-ttu-id="797fa-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="797fa-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="797fa-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="797fa-123">NOTES</span></span>

## <span data-ttu-id="797fa-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="797fa-124">RELATED LINKS</span></span>

[<span data-ttu-id="797fa-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="797fa-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)



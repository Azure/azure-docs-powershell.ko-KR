---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369202"
---
# <span data-ttu-id="4a423-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a423-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="4a423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a423-102">SYNOPSIS</span></span>
<span data-ttu-id="4a423-103">Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4a423-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a423-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a423-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a423-105">DESCRIPTION</span></span>
<span data-ttu-id="4a423-106">**Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet은 Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4a423-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a423-107">EXAMPLES</span></span>

### <span data-ttu-id="4a423-108">예제 1: 지정된 Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="4a423-109">이 명령은 지정된 Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="4a423-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a423-110">PARAMETERS</span></span>

### <span data-ttu-id="4a423-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a423-111">-DefaultProfile</span></span>
<span data-ttu-id="4a423-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a423-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a423-113">-Name</span></span>
<span data-ttu-id="4a423-114">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a423-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a423-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a423-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a423-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a423-117">CommonParameters</span></span>
<span data-ttu-id="4a423-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a423-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a423-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a423-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a423-120">입력</span><span class="sxs-lookup"><span data-stu-id="4a423-120">INPUTS</span></span>

### <span data-ttu-id="4a423-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4a423-121">System.String</span></span>

## <span data-ttu-id="4a423-122">출력</span><span class="sxs-lookup"><span data-stu-id="4a423-122">OUTPUTS</span></span>

### <span data-ttu-id="4a423-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a423-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="4a423-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a423-124">NOTES</span></span>

## <span data-ttu-id="4a423-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a423-125">RELATED LINKS</span></span>

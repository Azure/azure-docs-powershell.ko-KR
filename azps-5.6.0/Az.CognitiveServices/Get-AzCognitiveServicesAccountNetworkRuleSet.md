---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 60a61af31b5a7986779b19b893d4c02d0039ae49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007115"
---
# <span data-ttu-id="81194-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="81194-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="81194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81194-102">SYNOPSIS</span></span>
<span data-ttu-id="81194-103">Cognitive Services 계정의 NetworkRule 속성 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="81194-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="81194-104">구문</span><span class="sxs-lookup"><span data-stu-id="81194-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81194-105">설명</span><span class="sxs-lookup"><span data-stu-id="81194-105">DESCRIPTION</span></span>
<span data-ttu-id="81194-106">**Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet은 Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="81194-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="81194-107">예제</span><span class="sxs-lookup"><span data-stu-id="81194-107">EXAMPLES</span></span>

### <span data-ttu-id="81194-108">예제 1: 지정된 Cognitive Services 계정의 NetworkRule 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="81194-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="81194-109">이 명령은 지정된 Cognitive Services 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="81194-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="81194-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81194-110">PARAMETERS</span></span>

### <span data-ttu-id="81194-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81194-111">-DefaultProfile</span></span>
<span data-ttu-id="81194-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81194-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81194-113">-Name</span><span class="sxs-lookup"><span data-stu-id="81194-113">-Name</span></span>
<span data-ttu-id="81194-114">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81194-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="81194-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81194-115">-ResourceGroupName</span></span>
<span data-ttu-id="81194-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81194-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="81194-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81194-117">CommonParameters</span></span>
<span data-ttu-id="81194-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81194-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81194-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81194-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81194-120">입력</span><span class="sxs-lookup"><span data-stu-id="81194-120">INPUTS</span></span>

### <span data-ttu-id="81194-121">System.String</span><span class="sxs-lookup"><span data-stu-id="81194-121">System.String</span></span>

## <span data-ttu-id="81194-122">출력</span><span class="sxs-lookup"><span data-stu-id="81194-122">OUTPUTS</span></span>

### <span data-ttu-id="81194-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="81194-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="81194-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81194-124">NOTES</span></span>

## <span data-ttu-id="81194-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81194-125">RELATED LINKS</span></span>

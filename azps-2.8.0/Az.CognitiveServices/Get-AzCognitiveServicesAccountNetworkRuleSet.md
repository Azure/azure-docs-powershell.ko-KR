---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 99f591db004fe0c255b5d0ca836a470ff1e547a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697552"
---
# <span data-ttu-id="d4236-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4236-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d4236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4236-102">SYNOPSIS</span></span>
<span data-ttu-id="d4236-103">인지 서비스 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="d4236-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d4236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4236-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4236-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4236-105">DESCRIPTION</span></span>
<span data-ttu-id="d4236-106">**AzCognitiveServicesAccountNetworkRuleSet** Cmdlet은 인지 서비스 계정의 networkrule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d4236-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d4236-107">EXAMPLES</span></span>

### <span data-ttu-id="d4236-108">예제 1: 지정 된 인식 서비스 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="d4236-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="d4236-109">이 명령은 지정 된 인식 서비스 계정의 NetworkRule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="d4236-110">변수</span><span class="sxs-lookup"><span data-stu-id="d4236-110">PARAMETERS</span></span>

### <span data-ttu-id="d4236-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4236-111">-DefaultProfile</span></span>
<span data-ttu-id="d4236-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4236-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d4236-113">-Name</span></span>
<span data-ttu-id="d4236-114">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="d4236-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4236-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4236-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4236-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4236-117">CommonParameters</span></span>
<span data-ttu-id="d4236-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4236-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4236-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d4236-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4236-120">입력</span><span class="sxs-lookup"><span data-stu-id="d4236-120">INPUTS</span></span>

### <span data-ttu-id="d4236-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4236-121">System.String</span></span>

## <span data-ttu-id="d4236-122">출력</span><span class="sxs-lookup"><span data-stu-id="d4236-122">OUTPUTS</span></span>

### <span data-ttu-id="d4236-123">CognitiveServices. a m m 네트워크 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="d4236-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d4236-124">상속자</span><span class="sxs-lookup"><span data-stu-id="d4236-124">NOTES</span></span>

## <span data-ttu-id="d4236-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4236-125">RELATED LINKS</span></span>

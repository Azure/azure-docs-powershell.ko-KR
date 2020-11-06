---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530031"
---
# <span data-ttu-id="031ee-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="031ee-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="031ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="031ee-102">SYNOPSIS</span></span>
<span data-ttu-id="031ee-103">저장소 계정의 네트워크 규칙 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="031ee-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="031ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="031ee-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="031ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="031ee-105">DESCRIPTION</span></span>
<span data-ttu-id="031ee-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet은 저장소 계정의 networkrule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="031ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="031ee-107">EXAMPLES</span></span>

### <span data-ttu-id="031ee-108">예제 1: 지정 된 저장소 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="031ee-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="031ee-109">이 명령은 지정 된 저장소 계정의 NetworkRule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="031ee-110">변수</span><span class="sxs-lookup"><span data-stu-id="031ee-110">PARAMETERS</span></span>

### <span data-ttu-id="031ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031ee-111">-DefaultProfile</span></span>
<span data-ttu-id="031ee-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="031ee-113">-이름</span><span class="sxs-lookup"><span data-stu-id="031ee-113">-Name</span></span>
<span data-ttu-id="031ee-114">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="031ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="031ee-116">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="031ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031ee-117">CommonParameters</span></span>
<span data-ttu-id="031ee-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="031ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031ee-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031ee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031ee-120">입력</span><span class="sxs-lookup"><span data-stu-id="031ee-120">INPUTS</span></span>

### <span data-ttu-id="031ee-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="031ee-121">System.String</span></span>

## <span data-ttu-id="031ee-122">출력</span><span class="sxs-lookup"><span data-stu-id="031ee-122">OUTPUTS</span></span>

### <span data-ttu-id="031ee-123">Microsoft Azure.. m a. 모델. PSNetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="031ee-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="031ee-124">상속자</span><span class="sxs-lookup"><span data-stu-id="031ee-124">NOTES</span></span>

## <span data-ttu-id="031ee-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="031ee-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034708"
---
# <span data-ttu-id="50678-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="50678-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="50678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50678-102">SYNOPSIS</span></span>
<span data-ttu-id="50678-103">저장소 계정의 네트워크 규칙 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="50678-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="50678-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50678-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50678-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50678-105">DESCRIPTION</span></span>
<span data-ttu-id="50678-106">**AzStorageAccountNetworkRuleSet** Cmdlet은 저장소 계정의 networkrule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50678-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="50678-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50678-107">EXAMPLES</span></span>

### <span data-ttu-id="50678-108">예제 1: 지정 된 저장소 계정의 NetworkRule 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="50678-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="50678-109">이 명령은 지정 된 저장소 계정의 NetworkRule 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50678-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="50678-110">변수</span><span class="sxs-lookup"><span data-stu-id="50678-110">PARAMETERS</span></span>

### <span data-ttu-id="50678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50678-111">-DefaultProfile</span></span>
<span data-ttu-id="50678-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50678-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50678-113">-이름</span><span class="sxs-lookup"><span data-stu-id="50678-113">-Name</span></span>
<span data-ttu-id="50678-114">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50678-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="50678-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50678-115">-ResourceGroupName</span></span>
<span data-ttu-id="50678-116">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50678-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="50678-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50678-117">CommonParameters</span></span>
<span data-ttu-id="50678-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50678-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50678-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50678-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50678-120">입력</span><span class="sxs-lookup"><span data-stu-id="50678-120">INPUTS</span></span>

### <span data-ttu-id="50678-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50678-121">System.String</span></span>

## <span data-ttu-id="50678-122">출력</span><span class="sxs-lookup"><span data-stu-id="50678-122">OUTPUTS</span></span>

### <span data-ttu-id="50678-123">Microsoft Azure.. m a. 모델. PSNetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="50678-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="50678-124">상속자</span><span class="sxs-lookup"><span data-stu-id="50678-124">NOTES</span></span>

## <span data-ttu-id="50678-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50678-125">RELATED LINKS</span></span>

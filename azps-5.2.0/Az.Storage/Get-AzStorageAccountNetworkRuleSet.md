---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349701"
---
# <span data-ttu-id="1b5c6-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b5c6-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1b5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5c6-103">Storage 계정의 NetWorkRule 속성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="1b5c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b5c6-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b5c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b5c6-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5c6-106">**Get-AzStorageAccountNetworkRuleSet** cmdlet은 Storage 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="1b5c6-107">예제</span><span class="sxs-lookup"><span data-stu-id="1b5c6-107">EXAMPLES</span></span>

### <span data-ttu-id="1b5c6-108">예제 1: 지정된 Storage 계정의 NetworkRule 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="1b5c6-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="1b5c6-109">이 명령은 지정된 Storage 계정의 NetworkRule 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="1b5c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b5c6-110">PARAMETERS</span></span>

### <span data-ttu-id="1b5c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5c6-111">-DefaultProfile</span></span>
<span data-ttu-id="1b5c6-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b5c6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1b5c6-113">-Name</span></span>
<span data-ttu-id="1b5c6-114">Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1b5c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="1b5c6-116">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1b5c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5c6-117">CommonParameters</span></span>
<span data-ttu-id="1b5c6-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5c6-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b5c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5c6-120">입력</span><span class="sxs-lookup"><span data-stu-id="1b5c6-120">INPUTS</span></span>

### <span data-ttu-id="1b5c6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1b5c6-121">System.String</span></span>

## <span data-ttu-id="1b5c6-122">출력</span><span class="sxs-lookup"><span data-stu-id="1b5c6-122">OUTPUTS</span></span>

### <span data-ttu-id="1b5c6-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b5c6-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1b5c6-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b5c6-124">NOTES</span></span>

## <span data-ttu-id="1b5c6-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b5c6-125">RELATED LINKS</span></span>

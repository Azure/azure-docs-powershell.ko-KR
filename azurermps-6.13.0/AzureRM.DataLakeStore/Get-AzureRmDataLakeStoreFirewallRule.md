---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 191b1ebc1f83387a9cf1ac59f6fb3f7a55f115ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526199"
---
# <span data-ttu-id="75585-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="75585-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="75585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75585-102">SYNOPSIS</span></span>
<span data-ttu-id="75585-103">지정 된 Data Lake Store의 지정 된 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75585-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="75585-104">방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75585-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75585-105">구문과</span><span class="sxs-lookup"><span data-stu-id="75585-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75585-106">설명은</span><span class="sxs-lookup"><span data-stu-id="75585-106">DESCRIPTION</span></span>
<span data-ttu-id="75585-107">Get-AzureRmDataLakeStoreFirewallRule cmdlet은 지정 된 Data Lake Store에서 지정 된 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75585-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="75585-108">방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75585-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="75585-109">예제의</span><span class="sxs-lookup"><span data-stu-id="75585-109">EXAMPLES</span></span>

### <span data-ttu-id="75585-110">예제 1: 특정 방화벽 규칙 검색</span><span class="sxs-lookup"><span data-stu-id="75585-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="75585-111">"ContosoADL" 계정의 "MyFirewallRule" 방화벽 규칙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75585-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="75585-112">예제 2: 계정의 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="75585-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="75585-113">계정 "ContosoADL"의 모든 방화벽 규칙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75585-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="75585-114">변수</span><span class="sxs-lookup"><span data-stu-id="75585-114">PARAMETERS</span></span>

### <span data-ttu-id="75585-115">-계정</span><span class="sxs-lookup"><span data-stu-id="75585-115">-Account</span></span>
<span data-ttu-id="75585-116">방화벽 규칙을 검색할 Data Lake Store 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="75585-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75585-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75585-117">-DefaultProfile</span></span>
<span data-ttu-id="75585-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75585-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75585-119">-이름</span><span class="sxs-lookup"><span data-stu-id="75585-119">-Name</span></span>
<span data-ttu-id="75585-120">검색할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75585-120">The name of the firewall rule to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75585-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75585-121">-ResourceGroupName</span></span>
<span data-ttu-id="75585-122">지정 된 계정의 지정 된 방화벽 규칙을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75585-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75585-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75585-123">CommonParameters</span></span>
<span data-ttu-id="75585-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75585-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75585-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75585-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75585-126">입력</span><span class="sxs-lookup"><span data-stu-id="75585-126">INPUTS</span></span>

### <span data-ttu-id="75585-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75585-127">System.String</span></span>

## <span data-ttu-id="75585-128">출력</span><span class="sxs-lookup"><span data-stu-id="75585-128">OUTPUTS</span></span>

### <span data-ttu-id="75585-129">DataLakeStore. DataLakeStoreFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="75585-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="75585-130">상속자</span><span class="sxs-lookup"><span data-stu-id="75585-130">NOTES</span></span>

## <span data-ttu-id="75585-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75585-131">RELATED LINKS</span></span>

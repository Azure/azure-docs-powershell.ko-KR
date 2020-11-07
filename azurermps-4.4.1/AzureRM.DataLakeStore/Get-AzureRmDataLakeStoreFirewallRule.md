---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703756"
---
# <span data-ttu-id="abb68-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abb68-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="abb68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abb68-102">SYNOPSIS</span></span>
<span data-ttu-id="abb68-103">지정 된 Data Lake Store의 지정 된 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="abb68-104">방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb68-105">구문과</span><span class="sxs-lookup"><span data-stu-id="abb68-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb68-106">설명은</span><span class="sxs-lookup"><span data-stu-id="abb68-106">DESCRIPTION</span></span>
<span data-ttu-id="abb68-107">Get-AzureRmDataLakeStoreFirewallRule cmdlet은 지정 된 Data Lake Store에서 지정 된 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="abb68-108">방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="abb68-109">예제의</span><span class="sxs-lookup"><span data-stu-id="abb68-109">EXAMPLES</span></span>

### <span data-ttu-id="abb68-110">예제 1: 특정 방화벽 규칙 검색</span><span class="sxs-lookup"><span data-stu-id="abb68-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="abb68-111">"ContosoADL" 계정의 "MyFirewallRule" 방화벽 규칙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="abb68-112">예제 2: 계정의 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="abb68-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="abb68-113">계정 "ContosoADL"의 모든 방화벽 규칙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="abb68-114">변수</span><span class="sxs-lookup"><span data-stu-id="abb68-114">PARAMETERS</span></span>

### <span data-ttu-id="abb68-115">-계정</span><span class="sxs-lookup"><span data-stu-id="abb68-115">-Account</span></span>
<span data-ttu-id="abb68-116">방화벽 규칙을 검색할 Data Lake Store 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="abb68-117">-이름</span><span class="sxs-lookup"><span data-stu-id="abb68-117">-Name</span></span>
<span data-ttu-id="abb68-118">검색할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-118">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="abb68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb68-119">-ResourceGroupName</span></span>
<span data-ttu-id="abb68-120">지정 된 계정의 지정 된 방화벽 규칙을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="abb68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb68-121">-DefaultProfile</span></span>
<span data-ttu-id="abb68-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb68-123">CommonParameters</span></span>
<span data-ttu-id="abb68-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb68-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb68-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb68-126">입력</span><span class="sxs-lookup"><span data-stu-id="abb68-126">INPUTS</span></span>

## <span data-ttu-id="abb68-127">출력</span><span class="sxs-lookup"><span data-stu-id="abb68-127">OUTPUTS</span></span>

### <span data-ttu-id="abb68-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abb68-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="abb68-129">검색할 지정 된 방화벽 규칙</span><span class="sxs-lookup"><span data-stu-id="abb68-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="abb68-130">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="abb68-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="abb68-131">지정 된 계정에 있는 방화벽 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="abb68-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="abb68-132">상속자</span><span class="sxs-lookup"><span data-stu-id="abb68-132">NOTES</span></span>

## <span data-ttu-id="abb68-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abb68-133">RELATED LINKS</span></span>


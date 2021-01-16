---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341169"
---
# <span data-ttu-id="806cd-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="806cd-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="806cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="806cd-102">SYNOPSIS</span></span>
<span data-ttu-id="806cd-103">지정된 Data Lake Store에서 지정된 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="806cd-104">방화벽 규칙이 지정되지 않은 경우 계정에 대한 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="806cd-105">구문</span><span class="sxs-lookup"><span data-stu-id="806cd-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="806cd-106">설명</span><span class="sxs-lookup"><span data-stu-id="806cd-106">DESCRIPTION</span></span>
<span data-ttu-id="806cd-107">Get-AzDataLakeStoreFirewallRule cmdlet은 지정된 Data Lake Store에서 지정된 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="806cd-108">방화벽 규칙이 지정되지 않은 경우 계정에 대한 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="806cd-109">예제</span><span class="sxs-lookup"><span data-stu-id="806cd-109">EXAMPLES</span></span>

### <span data-ttu-id="806cd-110">예제 1: 특정 방화벽 규칙 검색</span><span class="sxs-lookup"><span data-stu-id="806cd-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="806cd-111">계정 "ContosoADL"에서 "MyFirewallRule"이라는 방화벽 규칙을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="806cd-112">예제 2: 계정의 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="806cd-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="806cd-113">"ContosoADL" 계정의 모든 방화벽 규칙을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="806cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="806cd-114">PARAMETERS</span></span>

### <span data-ttu-id="806cd-115">-Account</span><span class="sxs-lookup"><span data-stu-id="806cd-115">-Account</span></span>
<span data-ttu-id="806cd-116">방화벽 규칙을 검색할 Data Lake Store 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="806cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806cd-117">-DefaultProfile</span></span>
<span data-ttu-id="806cd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="806cd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="806cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="806cd-119">-Name</span></span>
<span data-ttu-id="806cd-120">검색할 방화벽 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="806cd-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="806cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="806cd-122">지정된 계정의 지정된 방화벽 규칙을 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="806cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806cd-123">CommonParameters</span></span>
<span data-ttu-id="806cd-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="806cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806cd-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="806cd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806cd-126">입력</span><span class="sxs-lookup"><span data-stu-id="806cd-126">INPUTS</span></span>

### <span data-ttu-id="806cd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="806cd-127">System.String</span></span>

## <span data-ttu-id="806cd-128">출력</span><span class="sxs-lookup"><span data-stu-id="806cd-128">OUTPUTS</span></span>

### <span data-ttu-id="806cd-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="806cd-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="806cd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="806cd-130">NOTES</span></span>

## <span data-ttu-id="806cd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="806cd-131">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 37c14547712233a025da56180e7a362f25168400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696924"
---
# <span data-ttu-id="1a8bd-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1a8bd-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="1a8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8bd-103">Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1a8bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a8bd-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a8bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="1a8bd-106">**AzDataLakeAnalyticsFirewallRule** Cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1a8bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="1a8bd-108">예제 1: 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="1a8bd-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="1a8bd-109">이 명령은 "ContosoAdlAcct" 계정의 "내 방화벽 규칙" 이라는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="1a8bd-110">예제 2: 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="1a8bd-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="1a8bd-111">이 명령은 "ContosoAdlAcct" 계정에서 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="1a8bd-112">변수</span><span class="sxs-lookup"><span data-stu-id="1a8bd-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8bd-113">-계정</span><span class="sxs-lookup"><span data-stu-id="1a8bd-113">-Account</span></span>
<span data-ttu-id="1a8bd-114">방화벽 규칙을 가져오는 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="1a8bd-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="1a8bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8bd-115">-DefaultProfile</span></span>
<span data-ttu-id="1a8bd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a8bd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a8bd-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1a8bd-117">-Name</span></span>
<span data-ttu-id="1a8bd-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="1a8bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a8bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a8bd-120">계정을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="1a8bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8bd-121">CommonParameters</span></span>
<span data-ttu-id="1a8bd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8bd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8bd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8bd-124">입력</span><span class="sxs-lookup"><span data-stu-id="1a8bd-124">INPUTS</span></span>

### <span data-ttu-id="1a8bd-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a8bd-125">System.String</span></span>

## <span data-ttu-id="1a8bd-126">출력</span><span class="sxs-lookup"><span data-stu-id="1a8bd-126">OUTPUTS</span></span>

### <span data-ttu-id="1a8bd-127">DataLakeAnalytics. DataLakeAnalyticsFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="1a8bd-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="1a8bd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="1a8bd-128">NOTES</span></span>

## <span data-ttu-id="1a8bd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a8bd-129">RELATED LINKS</span></span>
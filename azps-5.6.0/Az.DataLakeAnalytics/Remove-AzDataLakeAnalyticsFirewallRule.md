---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 31e4f1be594735d8ea7afbe9abc5f6ccb21ada1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957360"
---
# <span data-ttu-id="dd32e-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dd32e-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="dd32e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd32e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd32e-103">Data Lake Analytics 계정에서 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dd32e-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd32e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd32e-105">설명</span><span class="sxs-lookup"><span data-stu-id="dd32e-105">DESCRIPTION</span></span>
<span data-ttu-id="dd32e-106">**Remove-AzDataLakeAnalyticsFirewallRule** cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="dd32e-107">예제</span><span class="sxs-lookup"><span data-stu-id="dd32e-107">EXAMPLES</span></span>

### <span data-ttu-id="dd32e-108">예제 1: 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="dd32e-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="dd32e-109">이 명령은 계정 "ContosoAdlAcct"에서 "내 방화벽 규칙"이라는 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="dd32e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dd32e-110">PARAMETERS</span></span>

### <span data-ttu-id="dd32e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="dd32e-111">-Account</span></span>
<span data-ttu-id="dd32e-112">방화벽 규칙을 제거하기 위해 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="dd32e-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="dd32e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd32e-113">-DefaultProfile</span></span>
<span data-ttu-id="dd32e-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dd32e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd32e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dd32e-115">-Name</span></span>
<span data-ttu-id="dd32e-116">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="dd32e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd32e-117">-PassThru</span></span>
<span data-ttu-id="dd32e-118">삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd32e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd32e-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd32e-120">계정을 검색할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd32e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="dd32e-121">-Confirm</span></span>
<span data-ttu-id="dd32e-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd32e-123">-WhatIf</span></span>
<span data-ttu-id="dd32e-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd32e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd32e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd32e-126">CommonParameters</span></span>
<span data-ttu-id="dd32e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd32e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd32e-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dd32e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd32e-129">입력</span><span class="sxs-lookup"><span data-stu-id="dd32e-129">INPUTS</span></span>

### <span data-ttu-id="dd32e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dd32e-130">System.String</span></span>

### <span data-ttu-id="dd32e-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd32e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd32e-132">출력</span><span class="sxs-lookup"><span data-stu-id="dd32e-132">OUTPUTS</span></span>

### <span data-ttu-id="dd32e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd32e-133">System.Boolean</span></span>

## <span data-ttu-id="dd32e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd32e-134">NOTES</span></span>

## <span data-ttu-id="dd32e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd32e-135">RELATED LINKS</span></span>

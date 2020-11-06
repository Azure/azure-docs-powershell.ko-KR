---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: cca9a398ad216de1bb28aac128fd9642b79d2dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527619"
---
# <span data-ttu-id="549a1-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="549a1-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="549a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549a1-102">SYNOPSIS</span></span>
<span data-ttu-id="549a1-103">Data Lake Analytics 계정에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="549a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="549a1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="549a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="549a1-105">DESCRIPTION</span></span>
<span data-ttu-id="549a1-106">**AzureRmDataLakeAnalyticsFirewallRule** Cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="549a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="549a1-107">EXAMPLES</span></span>

### <span data-ttu-id="549a1-108">예제 1: 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="549a1-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="549a1-109">이 명령은 "ContosoAdlAcct" 계정의 "내 방화벽 규칙" 이라는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="549a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="549a1-110">PARAMETERS</span></span>

### <span data-ttu-id="549a1-111">-계정</span><span class="sxs-lookup"><span data-stu-id="549a1-111">-Account</span></span>
<span data-ttu-id="549a1-112">방화벽 규칙을 제거할 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="549a1-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="549a1-113">-이름</span><span class="sxs-lookup"><span data-stu-id="549a1-113">-Name</span></span>
<span data-ttu-id="549a1-114">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-114">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="549a1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="549a1-115">-PassThru</span></span>
<span data-ttu-id="549a1-116">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="549a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="549a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="549a1-118">계정을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="549a1-119">-확인</span><span class="sxs-lookup"><span data-stu-id="549a1-119">-Confirm</span></span>
<span data-ttu-id="549a1-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="549a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="549a1-121">-WhatIf</span></span>
<span data-ttu-id="549a1-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="549a1-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="549a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549a1-124">-DefaultProfile</span></span>
<span data-ttu-id="549a1-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="549a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549a1-126">CommonParameters</span></span>
<span data-ttu-id="549a1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="549a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549a1-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549a1-129">입력</span><span class="sxs-lookup"><span data-stu-id="549a1-129">INPUTS</span></span>

### <span data-ttu-id="549a1-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="549a1-130">System.String</span></span>
<span data-ttu-id="549a1-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="549a1-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="549a1-132">출력</span><span class="sxs-lookup"><span data-stu-id="549a1-132">OUTPUTS</span></span>

### <span data-ttu-id="549a1-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="549a1-133">System.Boolean</span></span>

## <span data-ttu-id="549a1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="549a1-134">NOTES</span></span>

## <span data-ttu-id="549a1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="549a1-135">RELATED LINKS</span></span>


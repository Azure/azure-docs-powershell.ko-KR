---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204349"
---
# <span data-ttu-id="03be6-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="03be6-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="03be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03be6-102">SYNOPSIS</span></span>
<span data-ttu-id="03be6-103">지정된 Data Lake Store에서 지정된 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="03be6-104">구문</span><span class="sxs-lookup"><span data-stu-id="03be6-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03be6-105">설명</span><span class="sxs-lookup"><span data-stu-id="03be6-105">DESCRIPTION</span></span>
<span data-ttu-id="03be6-106">**Remove-AzDataLakeStoreFirewallRule** cmdlet은 지정된 Data Lake Store에서 지정된 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="03be6-107">예제</span><span class="sxs-lookup"><span data-stu-id="03be6-107">EXAMPLES</span></span>

### <span data-ttu-id="03be6-108">예제 1: 계정에서 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="03be6-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="03be6-109">계정 "ContosoADL"에서 방화벽 규칙 "MyFirewallRule"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="03be6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03be6-110">PARAMETERS</span></span>

### <span data-ttu-id="03be6-111">-Account</span><span class="sxs-lookup"><span data-stu-id="03be6-111">-Account</span></span>
<span data-ttu-id="03be6-112">방화벽 규칙을 업데이트할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="03be6-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="03be6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03be6-113">-DefaultProfile</span></span>
<span data-ttu-id="03be6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03be6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03be6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="03be6-115">-Name</span></span>
<span data-ttu-id="03be6-116">삭제할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="03be6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03be6-117">-PassThru</span></span>
<span data-ttu-id="03be6-118">삭제 작업의 결과를 나타내는 부울 응답이 반환되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="03be6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03be6-119">-ResourceGroupName</span></span>
<span data-ttu-id="03be6-120">방화벽 규칙을 제거할 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03be6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03be6-121">-Confirm</span></span>
<span data-ttu-id="03be6-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03be6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03be6-123">-WhatIf</span></span>
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

### <span data-ttu-id="03be6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03be6-124">CommonParameters</span></span>
<span data-ttu-id="03be6-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03be6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03be6-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03be6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03be6-127">입력</span><span class="sxs-lookup"><span data-stu-id="03be6-127">INPUTS</span></span>

### <span data-ttu-id="03be6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="03be6-128">System.String</span></span>

### <span data-ttu-id="03be6-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03be6-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03be6-130">출력</span><span class="sxs-lookup"><span data-stu-id="03be6-130">OUTPUTS</span></span>

### <span data-ttu-id="03be6-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03be6-131">System.Boolean</span></span>

## <span data-ttu-id="03be6-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03be6-132">NOTES</span></span>

## <span data-ttu-id="03be6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03be6-133">RELATED LINKS</span></span>

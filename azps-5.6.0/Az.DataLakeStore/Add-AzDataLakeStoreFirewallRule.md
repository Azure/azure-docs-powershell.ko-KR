---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 60a3363716bb4e93efa02cc63d3e83548c4944f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004251"
---
# <span data-ttu-id="26022-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="26022-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="26022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26022-102">SYNOPSIS</span></span>
<span data-ttu-id="26022-103">지정된 Data Lake Store 계정에 방화벽 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="26022-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="26022-104">구문</span><span class="sxs-lookup"><span data-stu-id="26022-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26022-105">설명</span><span class="sxs-lookup"><span data-stu-id="26022-105">DESCRIPTION</span></span>
<span data-ttu-id="26022-106">**Add-AzDataLakeStoreFirewallRule** cmdlet은 지정된 Data Lake Store 계정에 방화벽 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="26022-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="26022-107">예제</span><span class="sxs-lookup"><span data-stu-id="26022-107">EXAMPLES</span></span>

### <span data-ttu-id="26022-108">예제 1: Data Lake Store 계정에 새 방화벽 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="26022-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="26022-109">이렇게 하면 IP 범위가 127.0.0.1 - 127.0.0.2인 계정 "ContosoADL"에 "MyRule"이라는 새 방화벽 규칙이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="26022-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="26022-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26022-110">PARAMETERS</span></span>

### <span data-ttu-id="26022-111">-Account</span><span class="sxs-lookup"><span data-stu-id="26022-111">-Account</span></span>
<span data-ttu-id="26022-112">방화벽 규칙을 추가하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="26022-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="26022-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26022-113">-DefaultProfile</span></span>
<span data-ttu-id="26022-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26022-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26022-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="26022-115">-EndIpAddress</span></span>
<span data-ttu-id="26022-116">방화벽 규칙에 대한 유효한 IP 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="26022-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26022-117">-Name</span><span class="sxs-lookup"><span data-stu-id="26022-117">-Name</span></span>
<span data-ttu-id="26022-118">추가할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26022-118">The name of the firewall rule to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26022-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26022-119">-ResourceGroupName</span></span>
<span data-ttu-id="26022-120">방화벽 규칙을 추가할 계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26022-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="26022-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="26022-121">-StartIpAddress</span></span>
<span data-ttu-id="26022-122">방화벽 규칙에 대한 유효한 IP 범위 시작</span><span class="sxs-lookup"><span data-stu-id="26022-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26022-123">-확인</span><span class="sxs-lookup"><span data-stu-id="26022-123">-Confirm</span></span>
<span data-ttu-id="26022-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26022-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26022-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26022-125">-WhatIf</span></span>
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

### <span data-ttu-id="26022-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26022-126">CommonParameters</span></span>
<span data-ttu-id="26022-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26022-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26022-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26022-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26022-129">입력</span><span class="sxs-lookup"><span data-stu-id="26022-129">INPUTS</span></span>

### <span data-ttu-id="26022-130">System.String</span><span class="sxs-lookup"><span data-stu-id="26022-130">System.String</span></span>

## <span data-ttu-id="26022-131">출력</span><span class="sxs-lookup"><span data-stu-id="26022-131">OUTPUTS</span></span>

### <span data-ttu-id="26022-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="26022-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="26022-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26022-133">NOTES</span></span>

## <span data-ttu-id="26022-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26022-134">RELATED LINKS</span></span>

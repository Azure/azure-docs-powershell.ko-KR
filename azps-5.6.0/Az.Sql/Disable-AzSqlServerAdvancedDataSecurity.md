---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967584"
---
# <span data-ttu-id="df448-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="df448-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="df448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df448-102">SYNOPSIS</span></span>
<span data-ttu-id="df448-103">서버에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="df448-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="df448-104">구문</span><span class="sxs-lookup"><span data-stu-id="df448-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df448-105">설명</span><span class="sxs-lookup"><span data-stu-id="df448-105">DESCRIPTION</span></span>
<span data-ttu-id="df448-106">**Disable-AzSqlServerAdvancedDataSecurity** cmdlet은 서버에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="df448-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="df448-107">예제</span><span class="sxs-lookup"><span data-stu-id="df448-107">EXAMPLES</span></span>

### <span data-ttu-id="df448-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="df448-108">Example 1</span></span>
### <span data-ttu-id="df448-109">예제 2: 서버 고급 데이터 보안을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="df448-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="df448-110">예제 3: 서버 리소스에서 서버 고급 데이터 보안을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="df448-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="df448-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df448-111">PARAMETERS</span></span>

### <span data-ttu-id="df448-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df448-112">-DefaultProfile</span></span>
<span data-ttu-id="df448-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df448-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df448-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df448-114">-InputObject</span></span>
<span data-ttu-id="df448-115">고급 데이터 보안 정책 작업과 함께 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="df448-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df448-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df448-116">-ResourceGroupName</span></span>
<span data-ttu-id="df448-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df448-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="df448-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df448-118">-ServerName</span></span>
<span data-ttu-id="df448-119">SQL 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df448-119">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df448-120">-확인</span><span class="sxs-lookup"><span data-stu-id="df448-120">-Confirm</span></span>
<span data-ttu-id="df448-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df448-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df448-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df448-122">-WhatIf</span></span>
<span data-ttu-id="df448-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="df448-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df448-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df448-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df448-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df448-125">CommonParameters</span></span>
<span data-ttu-id="df448-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df448-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df448-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df448-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df448-128">입력</span><span class="sxs-lookup"><span data-stu-id="df448-128">INPUTS</span></span>

### <span data-ttu-id="df448-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="df448-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="df448-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df448-130">System.String</span></span>

## <span data-ttu-id="df448-131">출력</span><span class="sxs-lookup"><span data-stu-id="df448-131">OUTPUTS</span></span>

### <span data-ttu-id="df448-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="df448-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="df448-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df448-133">NOTES</span></span>

## <span data-ttu-id="df448-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df448-134">RELATED LINKS</span></span>

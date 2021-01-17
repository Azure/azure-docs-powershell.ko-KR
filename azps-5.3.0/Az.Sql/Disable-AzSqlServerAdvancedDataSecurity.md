---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375285"
---
# <span data-ttu-id="a3e69-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="a3e69-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="a3e69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e69-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e69-103">서버에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="a3e69-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3e69-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3e69-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3e69-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e69-106">**Disable-AzSqlServerAdvancedDataSecurity** cmdlet은 서버에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="a3e69-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3e69-107">EXAMPLES</span></span>

### <span data-ttu-id="a3e69-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3e69-108">Example 1</span></span>
### <span data-ttu-id="a3e69-109">예제 2: 서버 고급 데이터 보안 사용 안</span><span class="sxs-lookup"><span data-stu-id="a3e69-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="a3e69-110">예제 3: 서버 리소스에서 서버 고급 데이터 보안 사용 안</span><span class="sxs-lookup"><span data-stu-id="a3e69-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="a3e69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3e69-111">PARAMETERS</span></span>

### <span data-ttu-id="a3e69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e69-112">-DefaultProfile</span></span>
<span data-ttu-id="a3e69-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3e69-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3e69-114">-InputObject</span></span>
<span data-ttu-id="a3e69-115">고급 데이터 보안 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="a3e69-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="a3e69-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e69-116">-ResourceGroupName</span></span>
<span data-ttu-id="a3e69-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3e69-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3e69-118">-ServerName</span></span>
<span data-ttu-id="a3e69-119">SQL 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="a3e69-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3e69-120">-Confirm</span></span>
<span data-ttu-id="a3e69-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3e69-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3e69-122">-WhatIf</span></span>
<span data-ttu-id="a3e69-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3e69-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3e69-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3e69-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e69-125">CommonParameters</span></span>
<span data-ttu-id="a3e69-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e69-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e69-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3e69-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e69-128">입력</span><span class="sxs-lookup"><span data-stu-id="a3e69-128">INPUTS</span></span>

### <span data-ttu-id="a3e69-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a3e69-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a3e69-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a3e69-130">System.String</span></span>

## <span data-ttu-id="a3e69-131">출력</span><span class="sxs-lookup"><span data-stu-id="a3e69-131">OUTPUTS</span></span>

### <span data-ttu-id="a3e69-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a3e69-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="a3e69-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3e69-133">NOTES</span></span>

## <span data-ttu-id="a3e69-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3e69-134">RELATED LINKS</span></span>

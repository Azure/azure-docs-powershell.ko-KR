---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304475"
---
# <span data-ttu-id="153d8-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="153d8-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="153d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="153d8-102">SYNOPSIS</span></span>
<span data-ttu-id="153d8-103">서버에서 고급 데이터 보안을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="153d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="153d8-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="153d8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="153d8-105">DESCRIPTION</span></span>
<span data-ttu-id="153d8-106">**AzSqlServerAdvancedDataSecurity** cmdlet은 서버에서 고급 데이터 보안을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="153d8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="153d8-107">EXAMPLES</span></span>

### <span data-ttu-id="153d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="153d8-108">Example 1</span></span>
### <span data-ttu-id="153d8-109">예제 2: 서버 고급 데이터 보안 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="153d8-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="153d8-110">예제 3: 서버 리소스에서 서버 고급 데이터 보안을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="153d8-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="153d8-111">변수</span><span class="sxs-lookup"><span data-stu-id="153d8-111">PARAMETERS</span></span>

### <span data-ttu-id="153d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153d8-112">-DefaultProfile</span></span>
<span data-ttu-id="153d8-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="153d8-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="153d8-114">-InputObject</span></span>
<span data-ttu-id="153d8-115">고급 데이터 보안 정책 작업에 사용할 서버 개체</span><span class="sxs-lookup"><span data-stu-id="153d8-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="153d8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="153d8-116">-ResourceGroupName</span></span>
<span data-ttu-id="153d8-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="153d8-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="153d8-118">-ServerName</span></span>
<span data-ttu-id="153d8-119">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="153d8-120">-확인</span><span class="sxs-lookup"><span data-stu-id="153d8-120">-Confirm</span></span>
<span data-ttu-id="153d8-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="153d8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="153d8-122">-WhatIf</span></span>
<span data-ttu-id="153d8-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="153d8-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="153d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153d8-125">CommonParameters</span></span>
<span data-ttu-id="153d8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="153d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153d8-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="153d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153d8-128">입력</span><span class="sxs-lookup"><span data-stu-id="153d8-128">INPUTS</span></span>

### <span data-ttu-id="153d8-129">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="153d8-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="153d8-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="153d8-130">System.String</span></span>

## <span data-ttu-id="153d8-131">출력</span><span class="sxs-lookup"><span data-stu-id="153d8-131">OUTPUTS</span></span>

### <span data-ttu-id="153d8-132">AdvancedThreatProtection. ServerAdvancedDataSecurityPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="153d8-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="153d8-133">상속자</span><span class="sxs-lookup"><span data-stu-id="153d8-133">NOTES</span></span>

## <span data-ttu-id="153d8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="153d8-134">RELATED LINKS</span></span>

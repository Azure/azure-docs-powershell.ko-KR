---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215188"
---
# <span data-ttu-id="6f8ed-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6f8ed-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="6f8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8ed-103">Azure SQL server의 감사 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="6f8ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f8ed-104">SYNTAX</span></span>

### <span data-ttu-id="6f8ed-105">ServerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f8ed-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8ed-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8ed-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f8ed-107">DESCRIPTION</span></span>
<span data-ttu-id="6f8ed-108">**AzSqlServerAudit** Cmdlet은 Azure SQL server의 감사 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="6f8ed-109">서버를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="6f8ed-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6f8ed-110">EXAMPLES</span></span>

### <span data-ttu-id="6f8ed-111">예제 1: Azure SQL server의 감사 설정 제거</span><span class="sxs-lookup"><span data-stu-id="6f8ed-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="6f8ed-112">예제 2: Azure SQL server의 감사 설정, 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="6f8ed-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="6f8ed-113">변수</span><span class="sxs-lookup"><span data-stu-id="6f8ed-113">PARAMETERS</span></span>

### <span data-ttu-id="6f8ed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f8ed-114">-AsJob</span></span>
<span data-ttu-id="6f8ed-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f8ed-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8ed-116">-DefaultProfile</span></span>
<span data-ttu-id="6f8ed-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f8ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="6f8ed-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8ed-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f8ed-120">-ServerName</span></span>
<span data-ttu-id="6f8ed-121">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8ed-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="6f8ed-122">-ServerObject</span></span>
<span data-ttu-id="6f8ed-123">감사 정책을 관리 하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8ed-124">-확인</span><span class="sxs-lookup"><span data-stu-id="6f8ed-124">-Confirm</span></span>
<span data-ttu-id="6f8ed-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8ed-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8ed-126">-WhatIf</span></span>
<span data-ttu-id="6f8ed-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f8ed-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8ed-129">CommonParameters</span></span>
<span data-ttu-id="6f8ed-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8ed-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f8ed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8ed-132">입력</span><span class="sxs-lookup"><span data-stu-id="6f8ed-132">INPUTS</span></span>

### <span data-ttu-id="6f8ed-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f8ed-133">System.String</span></span>

### <span data-ttu-id="6f8ed-134">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="6f8ed-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6f8ed-135">출력</span><span class="sxs-lookup"><span data-stu-id="6f8ed-135">OUTPUTS</span></span>

### <span data-ttu-id="6f8ed-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6f8ed-136">System.Boolean</span></span>

## <span data-ttu-id="6f8ed-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6f8ed-137">NOTES</span></span>

## <span data-ttu-id="6f8ed-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f8ed-138">RELATED LINKS</span></span>

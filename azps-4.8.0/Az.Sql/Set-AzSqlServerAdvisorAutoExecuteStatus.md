---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213864"
---
# <span data-ttu-id="cdd25-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="cdd25-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="cdd25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd25-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd25-103">Azure SQL Server Advisor의 자동 실행 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="cdd25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdd25-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cdd25-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd25-106">**Set-AzSqlServerAdvisorAutoExecuteStatus** Cmdlet은 Azure SQL Server Advisor에 대 한 자동 실행 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="cdd25-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cdd25-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd25-108">예제 1: 관리자에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="cdd25-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="cdd25-109">이 명령은 CreateIndex 라는 이름의 관리자의 자동 실행 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="cdd25-110">변수</span><span class="sxs-lookup"><span data-stu-id="cdd25-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd25-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="cdd25-111">-AdvisorName</span></span>
<span data-ttu-id="cdd25-112">이 cmdlet이 자동 실행 상태를 업데이트 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="cdd25-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="cdd25-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="cdd25-114">이 cmdlet이 자동 실행 상태를 업데이트 하는 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="cdd25-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cdd25-116">수</span><span class="sxs-lookup"><span data-stu-id="cdd25-116">Enabled</span></span>
- <span data-ttu-id="cdd25-117">비활성화</span><span class="sxs-lookup"><span data-stu-id="cdd25-117">Disabled</span></span>
- <span data-ttu-id="cdd25-118">기본값</span><span class="sxs-lookup"><span data-stu-id="cdd25-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd25-119">-DefaultProfile</span></span>
<span data-ttu-id="cdd25-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cdd25-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdd25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd25-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdd25-122">서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="cdd25-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cdd25-123">-ServerName</span></span>
<span data-ttu-id="cdd25-124">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cdd25-125">-확인</span><span class="sxs-lookup"><span data-stu-id="cdd25-125">-Confirm</span></span>
<span data-ttu-id="cdd25-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd25-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd25-127">-WhatIf</span></span>
<span data-ttu-id="cdd25-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd25-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd25-130">CommonParameters</span></span>
<span data-ttu-id="cdd25-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd25-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdd25-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd25-133">입력</span><span class="sxs-lookup"><span data-stu-id="cdd25-133">INPUTS</span></span>

### <span data-ttu-id="cdd25-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cdd25-134">System.String</span></span>

### <span data-ttu-id="cdd25-135">AdvisorAutoExecuteStatus을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="cdd25-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="cdd25-136">출력</span><span class="sxs-lookup"><span data-stu-id="cdd25-136">OUTPUTS</span></span>

### <span data-ttu-id="cdd25-137">AzureSqlServerAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="cdd25-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="cdd25-138">상속자</span><span class="sxs-lookup"><span data-stu-id="cdd25-138">NOTES</span></span>
* <span data-ttu-id="cdd25-139">키워드: azure, azurerm, arm, resource, 관리, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="cdd25-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="cdd25-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdd25-140">RELATED LINKS</span></span>

[<span data-ttu-id="cdd25-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="cdd25-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="cdd25-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="cdd25-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

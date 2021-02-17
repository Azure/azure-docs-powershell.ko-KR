---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178524"
---
# <span data-ttu-id="d1849-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="d1849-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="d1849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1849-102">SYNOPSIS</span></span>
<span data-ttu-id="d1849-103">데이터베이스에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="d1849-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1849-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1849-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1849-105">DESCRIPTION</span></span>
<span data-ttu-id="d1849-106">**Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet은 AzureAzure SQL 데이터베이스에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="d1849-107">이 cmdlet을 사용하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정하여 이 cmdlet이 설정을 제거하는 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="d1849-108">예제</span><span class="sxs-lookup"><span data-stu-id="d1849-108">EXAMPLES</span></span>

### <span data-ttu-id="d1849-109">예제 1: 데이터베이스에 대한 고급 위협 방지 설정 제거</span><span class="sxs-lookup"><span data-stu-id="d1849-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d1849-110">이 명령은 Server01이라는 서버의 Database01 데이터베이스에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d1849-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1849-111">PARAMETERS</span></span>

### <span data-ttu-id="d1849-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1849-112">-DatabaseName</span></span>
<span data-ttu-id="d1849-113">고급 위협 방지 설정을 제거해야 하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="d1849-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1849-114">-DefaultProfile</span></span>
<span data-ttu-id="d1849-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1849-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1849-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1849-116">-PassThru</span></span>
<span data-ttu-id="d1849-117">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d1849-118">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1849-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1849-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1849-120">서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="d1849-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1849-121">-ServerName</span></span>
<span data-ttu-id="d1849-122">데이터베이스가 실행되는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="d1849-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1849-123">-Confirm</span></span>
<span data-ttu-id="d1849-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1849-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1849-125">-WhatIf</span></span>
<span data-ttu-id="d1849-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1849-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1849-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1849-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1849-128">CommonParameters</span></span>
<span data-ttu-id="d1849-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1849-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1849-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1849-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1849-131">입력</span><span class="sxs-lookup"><span data-stu-id="d1849-131">INPUTS</span></span>

### <span data-ttu-id="d1849-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d1849-132">System.String</span></span>

## <span data-ttu-id="d1849-133">출력</span><span class="sxs-lookup"><span data-stu-id="d1849-133">OUTPUTS</span></span>

### <span data-ttu-id="d1849-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="d1849-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="d1849-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1849-135">NOTES</span></span>

## <span data-ttu-id="d1849-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1849-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1849-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d1849-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



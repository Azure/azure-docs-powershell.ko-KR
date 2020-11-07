---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698885"
---
# <span data-ttu-id="ff8cf-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ff8cf-101">New-AzSqlServer</span></span>

## <span data-ttu-id="ff8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8cf-103">SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="ff8cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff8cf-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff8cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff8cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8cf-106">**새 AzSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="ff8cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff8cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ff8cf-108">예제 1: 새 Azure SQL 데이터베이스 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ff8cf-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="ff8cf-109">이 명령은 버전 12 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="ff8cf-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff8cf-110">PARAMETERS</span></span>

### <span data-ttu-id="ff8cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff8cf-111">-AsJob</span></span>
<span data-ttu-id="ff8cf-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ff8cf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff8cf-113">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="ff8cf-113">-AssignIdentity</span></span>
<span data-ttu-id="ff8cf-114">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ff8cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8cf-115">-DefaultProfile</span></span>
<span data-ttu-id="ff8cf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff8cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff8cf-117">-위치</span><span class="sxs-lookup"><span data-stu-id="ff8cf-117">-Location</span></span>
<span data-ttu-id="ff8cf-118">이 cmdlet가 서버를 만드는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8cf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8cf-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff8cf-120">이 cmdlet에서 서버를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="ff8cf-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff8cf-121">-ServerName</span></span>
<span data-ttu-id="ff8cf-122">새 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-122">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8cf-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ff8cf-123">-ServerVersion</span></span>
<span data-ttu-id="ff8cf-124">새 서버의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-124">Specifies the version of the new server.</span></span> <span data-ttu-id="ff8cf-125">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="ff8cf-126">2.0를 지정 하 여 버전 11 서버를 만들거나, 12.0에서 버전 12 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8cf-127">-Sql관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="ff8cf-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="ff8cf-128">새 서버에 대 한 SQL 데이터베이스 서버 관리자 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="ff8cf-129">**PSCredential** 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="ff8cf-130">자세한 내용은을 입력 `Get-Help
Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8cf-131">태그</span><span class="sxs-lookup"><span data-stu-id="ff8cf-131">-Tags</span></span>
<span data-ttu-id="ff8cf-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ff8cf-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ff8cf-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8cf-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ff8cf-134">-Confirm</span></span>
<span data-ttu-id="ff8cf-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff8cf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff8cf-136">-WhatIf</span></span>
<span data-ttu-id="ff8cf-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff8cf-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff8cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8cf-139">CommonParameters</span></span>
<span data-ttu-id="ff8cf-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8cf-141">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff8cf-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8cf-142">입력</span><span class="sxs-lookup"><span data-stu-id="ff8cf-142">INPUTS</span></span>

### <span data-ttu-id="ff8cf-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff8cf-143">System.String</span></span>

## <span data-ttu-id="ff8cf-144">출력</span><span class="sxs-lookup"><span data-stu-id="ff8cf-144">OUTPUTS</span></span>

### <span data-ttu-id="ff8cf-145">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="ff8cf-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ff8cf-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ff8cf-146">NOTES</span></span>

## <span data-ttu-id="ff8cf-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff8cf-147">RELATED LINKS</span></span>

[<span data-ttu-id="ff8cf-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ff8cf-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="ff8cf-149">제거-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ff8cf-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="ff8cf-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ff8cf-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="ff8cf-151">새로운 AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ff8cf-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ff8cf-152">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ff8cf-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

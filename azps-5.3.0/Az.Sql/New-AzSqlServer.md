---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491590"
---
# <span data-ttu-id="43eee-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="43eee-101">New-AzSqlServer</span></span>

## <span data-ttu-id="43eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43eee-102">SYNOPSIS</span></span>
<span data-ttu-id="43eee-103">SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="43eee-104">구문</span><span class="sxs-lookup"><span data-stu-id="43eee-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43eee-105">설명</span><span class="sxs-lookup"><span data-stu-id="43eee-105">DESCRIPTION</span></span>
<span data-ttu-id="43eee-106">**New-AzSqlServer** cmdlet은 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="43eee-107">예제</span><span class="sxs-lookup"><span data-stu-id="43eee-107">EXAMPLES</span></span>

### <span data-ttu-id="43eee-108">예제 1: 새 Azure SQL 데이터베이스 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="43eee-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="43eee-109">이 명령은 버전 12 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="43eee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43eee-110">PARAMETERS</span></span>

### <span data-ttu-id="43eee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43eee-111">-AsJob</span></span>
<span data-ttu-id="43eee-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="43eee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43eee-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="43eee-113">-AssignIdentity</span></span>
<span data-ttu-id="43eee-114">Azure KeyVault와 같은 키 관리 서비스에서 사용할 이 서버에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="43eee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43eee-115">-DefaultProfile</span></span>
<span data-ttu-id="43eee-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43eee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43eee-117">-Location</span><span class="sxs-lookup"><span data-stu-id="43eee-117">-Location</span></span>
<span data-ttu-id="43eee-118">이 cmdlet이 서버를 만드는 데이터 센터의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="43eee-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="43eee-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="43eee-120">Sql Server에 적용할 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="43eee-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43eee-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="43eee-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="43eee-122">서버에 대한 공용 네트워크 액세스가 허용될지 여부를 지정하기 위해 플래그를 사용하도록 설정/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="43eee-123">사용하지 않도록 설정하면 개인 링크를 통해 만들어진 연결만 이 서버에 도달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="43eee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43eee-124">-ResourceGroupName</span></span>
<span data-ttu-id="43eee-125">이 cmdlet이 서버를 할당하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="43eee-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43eee-126">-ServerName</span></span>
<span data-ttu-id="43eee-127">새 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="43eee-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="43eee-128">-ServerVersion</span></span>
<span data-ttu-id="43eee-129">새 서버의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-129">Specifies the version of the new server.</span></span> <span data-ttu-id="43eee-130">이 매개 변수에 허용되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="43eee-131">2.0을 지정하여 버전 11 서버를 만들거나 12.0을 지정하여 버전 12 서버를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="43eee-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="43eee-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="43eee-133">새 서버에 SQL 데이터베이스 서버 관리자 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="43eee-134">**PSCredential** 개체를 얻습니다. Get-Credential cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="43eee-135">자세한 내용은 `Get-Help
Get-Credential` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-135">For more information, type `Get-Help
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

### <span data-ttu-id="43eee-136">-Tags</span><span class="sxs-lookup"><span data-stu-id="43eee-136">-Tags</span></span>
<span data-ttu-id="43eee-137">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="43eee-138">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="43eee-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="43eee-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43eee-139">-Confirm</span></span>
<span data-ttu-id="43eee-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43eee-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43eee-141">-WhatIf</span></span>
<span data-ttu-id="43eee-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43eee-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43eee-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43eee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43eee-144">CommonParameters</span></span>
<span data-ttu-id="43eee-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43eee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43eee-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43eee-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43eee-147">입력</span><span class="sxs-lookup"><span data-stu-id="43eee-147">INPUTS</span></span>

### <span data-ttu-id="43eee-148">System.String</span><span class="sxs-lookup"><span data-stu-id="43eee-148">System.String</span></span>

## <span data-ttu-id="43eee-149">출력</span><span class="sxs-lookup"><span data-stu-id="43eee-149">OUTPUTS</span></span>

### <span data-ttu-id="43eee-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="43eee-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="43eee-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43eee-151">NOTES</span></span>

## <span data-ttu-id="43eee-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43eee-152">RELATED LINKS</span></span>

[<span data-ttu-id="43eee-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="43eee-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="43eee-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="43eee-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="43eee-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="43eee-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="43eee-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="43eee-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="43eee-157">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="43eee-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

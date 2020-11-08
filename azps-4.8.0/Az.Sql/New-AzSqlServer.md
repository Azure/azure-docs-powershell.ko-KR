---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048641"
---
# <span data-ttu-id="72d66-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72d66-101">New-AzSqlServer</span></span>

## <span data-ttu-id="72d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d66-102">SYNOPSIS</span></span>
<span data-ttu-id="72d66-103">SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="72d66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72d66-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72d66-105">DESCRIPTION</span></span>
<span data-ttu-id="72d66-106">**새 AzSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="72d66-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72d66-107">EXAMPLES</span></span>

### <span data-ttu-id="72d66-108">예제 1: 새 Azure SQL 데이터베이스 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="72d66-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="72d66-109">이 명령은 버전 12 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="72d66-110">변수</span><span class="sxs-lookup"><span data-stu-id="72d66-110">PARAMETERS</span></span>

### <span data-ttu-id="72d66-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72d66-111">-AsJob</span></span>
<span data-ttu-id="72d66-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="72d66-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72d66-113">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="72d66-113">-AssignIdentity</span></span>
<span data-ttu-id="72d66-114">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="72d66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d66-115">-DefaultProfile</span></span>
<span data-ttu-id="72d66-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72d66-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72d66-117">-위치</span><span class="sxs-lookup"><span data-stu-id="72d66-117">-Location</span></span>
<span data-ttu-id="72d66-118">이 cmdlet가 서버를 만드는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="72d66-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="72d66-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="72d66-120">Sql Server에 적용 되는 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="72d66-120">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="72d66-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="72d66-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="72d66-122">설정/해제 플래그를 사용 하 여 서버에 대 한 공용 네트워크 액세스 허용 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="72d66-123">이 기능을 사용 하지 않도록 설정 하면 비공개 링크를 통해 생성 된 연결만이 서버에 도달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="72d66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d66-124">-ResourceGroupName</span></span>
<span data-ttu-id="72d66-125">이 cmdlet에서 서버를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="72d66-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72d66-126">-ServerName</span></span>
<span data-ttu-id="72d66-127">새 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="72d66-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="72d66-128">-ServerVersion</span></span>
<span data-ttu-id="72d66-129">새 서버의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-129">Specifies the version of the new server.</span></span> <span data-ttu-id="72d66-130">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="72d66-131">2.0를 지정 하 여 버전 11 서버를 만들거나, 12.0에서 버전 12 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="72d66-132">-Sql관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="72d66-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="72d66-133">새 서버에 대 한 SQL 데이터베이스 서버 관리자 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="72d66-134">**PSCredential** 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="72d66-135">자세한 내용은을 입력 `Get-Help
Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="72d66-135">For more information, type `Get-Help
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

### <span data-ttu-id="72d66-136">태그</span><span class="sxs-lookup"><span data-stu-id="72d66-136">-Tags</span></span>
<span data-ttu-id="72d66-137">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72d66-138">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="72d66-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72d66-139">-확인</span><span class="sxs-lookup"><span data-stu-id="72d66-139">-Confirm</span></span>
<span data-ttu-id="72d66-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d66-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d66-141">-WhatIf</span></span>
<span data-ttu-id="72d66-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d66-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d66-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d66-144">CommonParameters</span></span>
<span data-ttu-id="72d66-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d66-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d66-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="72d66-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d66-147">입력</span><span class="sxs-lookup"><span data-stu-id="72d66-147">INPUTS</span></span>

### <span data-ttu-id="72d66-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72d66-148">System.String</span></span>

## <span data-ttu-id="72d66-149">출력</span><span class="sxs-lookup"><span data-stu-id="72d66-149">OUTPUTS</span></span>

### <span data-ttu-id="72d66-150">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="72d66-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="72d66-151">상속자</span><span class="sxs-lookup"><span data-stu-id="72d66-151">NOTES</span></span>

## <span data-ttu-id="72d66-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72d66-152">RELATED LINKS</span></span>

[<span data-ttu-id="72d66-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72d66-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="72d66-154">제거-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72d66-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="72d66-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72d66-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="72d66-156">새로운 AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72d66-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="72d66-157">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="72d66-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

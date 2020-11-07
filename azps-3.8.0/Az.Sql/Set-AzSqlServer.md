---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877554"
---
# <span data-ttu-id="20440-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="20440-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="20440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20440-102">SYNOPSIS</span></span>
<span data-ttu-id="20440-103">SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="20440-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20440-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20440-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20440-105">DESCRIPTION</span></span>
<span data-ttu-id="20440-106">**AzSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="20440-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20440-107">EXAMPLES</span></span>

### <span data-ttu-id="20440-108">예제 1: 관리자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="20440-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="20440-109">이 명령은 server01 이라는 AzureSQL 서버에서 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="20440-110">변수</span><span class="sxs-lookup"><span data-stu-id="20440-110">PARAMETERS</span></span>

### <span data-ttu-id="20440-111">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="20440-111">-AssignIdentity</span></span>
<span data-ttu-id="20440-112">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="20440-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20440-113">-DefaultProfile</span></span>
<span data-ttu-id="20440-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20440-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20440-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20440-115">-Force</span></span>
<span data-ttu-id="20440-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20440-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="20440-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="20440-118">설정/해제 플래그를 사용 하 여 서버에 대 한 공용 네트워크 액세스 허용 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="20440-119">이 기능을 사용 하지 않도록 설정 하면 비공개 링크를 통해 생성 된 연결만이 서버에 도달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20440-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20440-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20440-120">-ResourceGroupName</span></span>
<span data-ttu-id="20440-121">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="20440-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20440-122">-ServerName</span></span>
<span data-ttu-id="20440-123">이 cmdlet이 수정 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20440-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="20440-124">-ServerVersion</span></span>
<span data-ttu-id="20440-125">이 cmdlet이 서버를 변경할 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="20440-126">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="20440-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="20440-127">-Sql관리자 암호</span><span class="sxs-lookup"><span data-stu-id="20440-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="20440-128">데이터베이스 서버 관리자의 새 암호를 **SecureString** 으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="20440-129">**SecureString** 을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="20440-130">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="20440-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20440-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="20440-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="20440-132">Sql Server에 적용 되는 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="20440-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="20440-133">태그</span><span class="sxs-lookup"><span data-stu-id="20440-133">-Tags</span></span>
<span data-ttu-id="20440-134">이 cmdlet이 서버와 연결 하는 태그 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="20440-135">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="20440-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="20440-136">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="20440-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20440-137">-확인</span><span class="sxs-lookup"><span data-stu-id="20440-137">-Confirm</span></span>
<span data-ttu-id="20440-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20440-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20440-139">-WhatIf</span></span>
<span data-ttu-id="20440-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20440-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20440-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20440-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20440-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20440-142">CommonParameters</span></span>
<span data-ttu-id="20440-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20440-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20440-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20440-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20440-145">입력</span><span class="sxs-lookup"><span data-stu-id="20440-145">INPUTS</span></span>

### <span data-ttu-id="20440-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20440-146">System.String</span></span>

## <span data-ttu-id="20440-147">출력</span><span class="sxs-lookup"><span data-stu-id="20440-147">OUTPUTS</span></span>

### <span data-ttu-id="20440-148">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="20440-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="20440-149">상속자</span><span class="sxs-lookup"><span data-stu-id="20440-149">NOTES</span></span>

## <span data-ttu-id="20440-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20440-150">RELATED LINKS</span></span>

[<span data-ttu-id="20440-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="20440-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

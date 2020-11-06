---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: e385d51a1fba06857b922ab9aabbd100e61b036e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534184"
---
# <span data-ttu-id="ece95-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="ece95-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="ece95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece95-102">SYNOPSIS</span></span>
<span data-ttu-id="ece95-103">SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ece95-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ece95-105">DESCRIPTION</span></span>
<span data-ttu-id="ece95-106">**AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="ece95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ece95-107">EXAMPLES</span></span>

### <span data-ttu-id="ece95-108">예제 1: 관리자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="ece95-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
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

<span data-ttu-id="ece95-109">이 명령은 server01 이라는 AzureSQL 서버에서 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="ece95-110">변수</span><span class="sxs-lookup"><span data-stu-id="ece95-110">PARAMETERS</span></span>

### <span data-ttu-id="ece95-111">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="ece95-111">-AssignIdentity</span></span>
<span data-ttu-id="ece95-112">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ece95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece95-113">-DefaultProfile</span></span>
<span data-ttu-id="ece95-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ece95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece95-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ece95-115">-Force</span></span>
<span data-ttu-id="ece95-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ece95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece95-117">-ResourceGroupName</span></span>
<span data-ttu-id="ece95-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ece95-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ece95-119">-ServerName</span></span>
<span data-ttu-id="ece95-120">이 cmdlet이 수정 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-120">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ece95-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ece95-121">-ServerVersion</span></span>
<span data-ttu-id="ece95-122">이 cmdlet이 서버를 변경할 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="ece95-123">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="ece95-124">-Sql관리자 암호</span><span class="sxs-lookup"><span data-stu-id="ece95-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="ece95-125">데이터베이스 서버 관리자의 새 암호를 **SecureString** 으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="ece95-126">**SecureString** 을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="ece95-127">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="ece95-127">For more information, type `Get-Help
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

### <span data-ttu-id="ece95-128">태그</span><span class="sxs-lookup"><span data-stu-id="ece95-128">-Tags</span></span>
<span data-ttu-id="ece95-129">이 cmdlet이 서버와 연결 하는 태그 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="ece95-130">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ece95-131">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ece95-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ece95-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ece95-132">-Confirm</span></span>
<span data-ttu-id="ece95-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece95-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece95-134">-WhatIf</span></span>
<span data-ttu-id="ece95-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece95-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece95-137">CommonParameters</span></span>
<span data-ttu-id="ece95-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece95-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece95-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece95-140">입력</span><span class="sxs-lookup"><span data-stu-id="ece95-140">INPUTS</span></span>

### <span data-ttu-id="ece95-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ece95-141">System.String</span></span>

## <span data-ttu-id="ece95-142">출력</span><span class="sxs-lookup"><span data-stu-id="ece95-142">OUTPUTS</span></span>

### <span data-ttu-id="ece95-143">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="ece95-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ece95-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ece95-144">NOTES</span></span>

## <span data-ttu-id="ece95-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ece95-145">RELATED LINKS</span></span>

[<span data-ttu-id="ece95-146">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ece95-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

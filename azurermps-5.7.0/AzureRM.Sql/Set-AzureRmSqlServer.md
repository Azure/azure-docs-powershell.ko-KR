---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: f7d6dab2629dc8247cb404d1de2dc58b21fc8a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534555"
---
# <span data-ttu-id="41a53-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="41a53-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="41a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41a53-102">SYNOPSIS</span></span>
<span data-ttu-id="41a53-103">SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41a53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41a53-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41a53-105">DESCRIPTION</span></span>
<span data-ttu-id="41a53-106">**AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="41a53-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41a53-107">EXAMPLES</span></span>

### <span data-ttu-id="41a53-108">예제 1: 관리자 암호 다시 설정</span><span class="sxs-lookup"><span data-stu-id="41a53-108">Example 1: Reset the administrator password</span></span>
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

<span data-ttu-id="41a53-109">이 명령은 server01 이라는 AzureSQL 서버에서 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="41a53-110">변수</span><span class="sxs-lookup"><span data-stu-id="41a53-110">PARAMETERS</span></span>

### <span data-ttu-id="41a53-111">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="41a53-111">-AssignIdentity</span></span>
<span data-ttu-id="41a53-112">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a53-113">-DefaultProfile</span></span>
<span data-ttu-id="41a53-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="41a53-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41a53-115">-Force</span></span>
<span data-ttu-id="41a53-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a53-117">-ResourceGroupName</span></span>
<span data-ttu-id="41a53-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41a53-119">-ServerName</span></span>
<span data-ttu-id="41a53-120">이 cmdlet이 수정 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="41a53-121">-ServerVersion</span></span>
<span data-ttu-id="41a53-122">이 cmdlet이 서버를 변경할 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="41a53-123">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="41a53-124">-Sql관리자 암호</span><span class="sxs-lookup"><span data-stu-id="41a53-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="41a53-125">데이터베이스 서버 관리자의 새 암호를 **SecureString** 으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="41a53-126">**SecureString** 을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="41a53-127">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="41a53-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-128">태그</span><span class="sxs-lookup"><span data-stu-id="41a53-128">-Tags</span></span>
<span data-ttu-id="41a53-129">이 cmdlet이 서버와 연결 하는 태그 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="41a53-130">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="41a53-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="41a53-131">For example:</span></span>

<span data-ttu-id="41a53-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="41a53-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-133">-확인</span><span class="sxs-lookup"><span data-stu-id="41a53-133">-Confirm</span></span>
<span data-ttu-id="41a53-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a53-135">-WhatIf</span></span>
<span data-ttu-id="41a53-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a53-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a53-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a53-138">CommonParameters</span></span>
<span data-ttu-id="41a53-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a53-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a53-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a53-141">입력</span><span class="sxs-lookup"><span data-stu-id="41a53-141">INPUTS</span></span>

### <span data-ttu-id="41a53-142">않아야</span><span class="sxs-lookup"><span data-stu-id="41a53-142">None</span></span>
<span data-ttu-id="41a53-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41a53-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41a53-144">출력</span><span class="sxs-lookup"><span data-stu-id="41a53-144">OUTPUTS</span></span>

### <span data-ttu-id="41a53-145">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="41a53-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="41a53-146">상속자</span><span class="sxs-lookup"><span data-stu-id="41a53-146">NOTES</span></span>

## <span data-ttu-id="41a53-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41a53-147">RELATED LINKS</span></span>

[<span data-ttu-id="41a53-148">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="41a53-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702830"
---
# <span data-ttu-id="c1826-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c1826-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="c1826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1826-102">SYNOPSIS</span></span>
<span data-ttu-id="c1826-103">SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1826-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1826-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1826-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1826-105">DESCRIPTION</span></span>
<span data-ttu-id="c1826-106">**새 AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="c1826-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1826-107">EXAMPLES</span></span>

### <span data-ttu-id="c1826-108">예제 1: 새 Azure SQL 데이터베이스 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="c1826-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="c1826-109">이 명령은 버전 12 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="c1826-110">변수</span><span class="sxs-lookup"><span data-stu-id="c1826-110">PARAMETERS</span></span>

### <span data-ttu-id="c1826-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1826-111">-AsJob</span></span>
<span data-ttu-id="c1826-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c1826-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="c1826-113">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="c1826-113">-AssignIdentity</span></span>
<span data-ttu-id="c1826-114">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c1826-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1826-115">-DefaultProfile</span></span>
<span data-ttu-id="c1826-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c1826-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1826-117">-위치</span><span class="sxs-lookup"><span data-stu-id="c1826-117">-Location</span></span>
<span data-ttu-id="c1826-118">이 cmdlet가 서버를 만드는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1826-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1826-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1826-120">이 cmdlet에서 서버를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="c1826-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1826-121">-ServerName</span></span>
<span data-ttu-id="c1826-122">새 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1826-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c1826-123">-ServerVersion</span></span>
<span data-ttu-id="c1826-124">새 서버의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-124">Specifies the version of the new server.</span></span> <span data-ttu-id="c1826-125">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="c1826-126">2.0를 지정 하 여 버전 11 서버를 만들거나, 12.0에서 버전 12 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="c1826-127">-Sql관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="c1826-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="c1826-128">새 서버에 대 한 SQL 데이터베이스 서버 관리자 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="c1826-129">**PSCredential** 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="c1826-130">자세한 내용은을 입력 `Get-Help
Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1826-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1826-131">태그</span><span class="sxs-lookup"><span data-stu-id="c1826-131">-Tags</span></span>
<span data-ttu-id="c1826-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c1826-133">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c1826-133">For example:</span></span>

<span data-ttu-id="c1826-134">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c1826-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c1826-135">-확인</span><span class="sxs-lookup"><span data-stu-id="c1826-135">-Confirm</span></span>
<span data-ttu-id="c1826-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1826-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1826-137">-WhatIf</span></span>
<span data-ttu-id="c1826-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1826-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1826-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1826-140">CommonParameters</span></span>
<span data-ttu-id="c1826-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1826-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1826-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1826-143">입력</span><span class="sxs-lookup"><span data-stu-id="c1826-143">INPUTS</span></span>

### <span data-ttu-id="c1826-144">않아야</span><span class="sxs-lookup"><span data-stu-id="c1826-144">None</span></span>
<span data-ttu-id="c1826-145">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1826-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1826-146">출력</span><span class="sxs-lookup"><span data-stu-id="c1826-146">OUTPUTS</span></span>

### <span data-ttu-id="c1826-147">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="c1826-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c1826-148">상속자</span><span class="sxs-lookup"><span data-stu-id="c1826-148">NOTES</span></span>

## <span data-ttu-id="c1826-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1826-149">RELATED LINKS</span></span>

[<span data-ttu-id="c1826-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c1826-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="c1826-151">제거-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c1826-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="c1826-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c1826-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="c1826-153">새로운 AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1826-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c1826-154">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c1826-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

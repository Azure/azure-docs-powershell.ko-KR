---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703094"
---
# <span data-ttu-id="790d1-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="790d1-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="790d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790d1-102">SYNOPSIS</span></span>
<span data-ttu-id="790d1-103">SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="790d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="790d1-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="790d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="790d1-105">DESCRIPTION</span></span>
<span data-ttu-id="790d1-106">**새 AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="790d1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="790d1-107">EXAMPLES</span></span>

### <span data-ttu-id="790d1-108">예제 1: 새 Azure SQL 데이터베이스 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="790d1-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="790d1-109">이 명령은 버전 12 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="790d1-110">변수</span><span class="sxs-lookup"><span data-stu-id="790d1-110">PARAMETERS</span></span>

### <span data-ttu-id="790d1-111">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="790d1-111">-AssignIdentity</span></span>
<span data-ttu-id="790d1-112">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="790d1-113">-위치</span><span class="sxs-lookup"><span data-stu-id="790d1-113">-Location</span></span>
<span data-ttu-id="790d1-114">이 cmdlet가 서버를 만드는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="790d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="790d1-116">이 cmdlet에서 서버를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="790d1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="790d1-117">-ServerName</span></span>
<span data-ttu-id="790d1-118">새 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="790d1-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="790d1-119">-ServerVersion</span></span>
<span data-ttu-id="790d1-120">새 서버의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-120">Specifies the version of the new server.</span></span> <span data-ttu-id="790d1-121">이 매개 변수에 허용 되는 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="790d1-122">2.0를 지정 하 여 버전 11 서버를 만들거나, 12.0에서 버전 12 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="790d1-123">-Sql관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="790d1-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="790d1-124">새 서버에 대 한 SQL 데이터베이스 서버 관리자 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="790d1-125">**PSCredential** 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="790d1-126">자세한 내용은을 입력 `Get-Help
Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="790d1-126">For more information, type `Get-Help
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

### <span data-ttu-id="790d1-127">태그</span><span class="sxs-lookup"><span data-stu-id="790d1-127">-Tags</span></span>
<span data-ttu-id="790d1-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="790d1-129">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="790d1-129">For example:</span></span>

<span data-ttu-id="790d1-130">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="790d1-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="790d1-131">-확인</span><span class="sxs-lookup"><span data-stu-id="790d1-131">-Confirm</span></span>
<span data-ttu-id="790d1-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="790d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="790d1-133">-WhatIf</span></span>
<span data-ttu-id="790d1-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="790d1-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="790d1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790d1-136">-DefaultProfile</span></span>
<span data-ttu-id="790d1-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="790d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790d1-138">CommonParameters</span></span>
<span data-ttu-id="790d1-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790d1-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790d1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790d1-141">입력</span><span class="sxs-lookup"><span data-stu-id="790d1-141">INPUTS</span></span>

## <span data-ttu-id="790d1-142">출력</span><span class="sxs-lookup"><span data-stu-id="790d1-142">OUTPUTS</span></span>

### <span data-ttu-id="790d1-143">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="790d1-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="790d1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="790d1-144">NOTES</span></span>

## <span data-ttu-id="790d1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="790d1-145">RELATED LINKS</span></span>

[<span data-ttu-id="790d1-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="790d1-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="790d1-147">제거-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="790d1-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="790d1-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="790d1-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="790d1-149">새로운 AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="790d1-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="790d1-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="790d1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

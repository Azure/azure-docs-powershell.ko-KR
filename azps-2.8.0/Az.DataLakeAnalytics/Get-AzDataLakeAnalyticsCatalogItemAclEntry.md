---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e004ac5d14b10ac2304a937cb029361524fc829e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696925"
---
# <span data-ttu-id="25a64-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="25a64-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="25a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a64-102">SYNOPSIS</span></span>
<span data-ttu-id="25a64-103">Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL에 있는 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="25a64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25a64-104">SYNTAX</span></span>

### <span data-ttu-id="25a64-105">GetCatalogAclEntry (기본값)</span><span class="sxs-lookup"><span data-stu-id="25a64-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25a64-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a64-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a64-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="25a64-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a64-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a64-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a64-111">설명은</span><span class="sxs-lookup"><span data-stu-id="25a64-111">DESCRIPTION</span></span>
<span data-ttu-id="25a64-112">**AzDataLakeAnalyticsCatalogItemAclEntry** Cmdlet은 Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL (액세스 제어 목록)에 있는 항목 (ace) 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="25a64-113">예제의</span><span class="sxs-lookup"><span data-stu-id="25a64-113">EXAMPLES</span></span>

### <span data-ttu-id="25a64-114">예제 1: 카탈로그에 대 한 ACL 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="25a64-115">이 명령은 지정 된 Data Lake Analytics 계정의 카탈로그에 대 한 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="25a64-116">예제 2: 카탈로그에 대 한 사용자 소유자의 ACL 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="25a64-117">이 명령은 지정 된 Data Lake Analytics 계정의 카탈로그에 대 한 사용자 소유자의 ACL 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="25a64-118">예제 3: 카탈로그에 대 한 그룹 소유자의 ACL 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="25a64-119">이 명령은 지정 된 Data Lake Analytics 계정 카탈로그에 대 한 그룹 소유자의 ACL 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="25a64-120">예제 4: 데이터베이스의 ACL 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="25a64-121">이 명령은 지정 된 Data Lake Analytics 계정의 데이터베이스에 대 한 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="25a64-122">예제 5: 데이터베이스에 대 한 사용자 소유자의 ACL 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="25a64-123">이 명령은 지정 된 Data Lake Analytics 계정 데이터베이스의 사용자 소유자에 대 한 ACL 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="25a64-124">예제 6: 데이터베이스의 그룹 소유자에 대 한 ACL 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="25a64-125">이 명령은 지정 된 Data Lake Analytics 계정 데이터베이스에 대 한 그룹 소유자의 ACL 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="25a64-126">변수</span><span class="sxs-lookup"><span data-stu-id="25a64-126">PARAMETERS</span></span>

### <span data-ttu-id="25a64-127">-계정</span><span class="sxs-lookup"><span data-stu-id="25a64-127">-Account</span></span>
<span data-ttu-id="25a64-128">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-128">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a64-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a64-129">-DefaultProfile</span></span>
<span data-ttu-id="25a64-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a64-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-131">-GroupOwner</span></span>
<span data-ttu-id="25a64-132">그룹 소유자 용 카탈로그의 ACL 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="25a64-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a64-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="25a64-133">-ItemType</span></span>
<span data-ttu-id="25a64-134">카탈로그 또는 카탈로그 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="25a64-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25a64-136">카탈로그인</span><span class="sxs-lookup"><span data-stu-id="25a64-136">Catalog</span></span>
- <span data-ttu-id="25a64-137">데이터</span><span class="sxs-lookup"><span data-stu-id="25a64-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a64-138">-Path</span><span class="sxs-lookup"><span data-stu-id="25a64-138">-Path</span></span>
<span data-ttu-id="25a64-139">카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="25a64-140">경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a64-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="25a64-141">-UserOwner</span></span>
<span data-ttu-id="25a64-142">사용자 소유자 용 카탈로그의 ACL 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a64-143">CommonParameters</span></span>
<span data-ttu-id="25a64-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a64-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a64-146">입력</span><span class="sxs-lookup"><span data-stu-id="25a64-146">INPUTS</span></span>

### <span data-ttu-id="25a64-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25a64-147">System.String</span></span>

### <span data-ttu-id="25a64-148">DataLakeAnalytics. CatalogPathInstance/.</span><span class="sxs-lookup"><span data-stu-id="25a64-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="25a64-149">출력</span><span class="sxs-lookup"><span data-stu-id="25a64-149">OUTPUTS</span></span>

### <span data-ttu-id="25a64-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="25a64-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="25a64-151">상속자</span><span class="sxs-lookup"><span data-stu-id="25a64-151">NOTES</span></span>

## <span data-ttu-id="25a64-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25a64-152">RELATED LINKS</span></span>

[<span data-ttu-id="25a64-153">U-SQL은 이제 데이터베이스 수준 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a64-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="25a64-154">제거-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="25a64-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="25a64-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="25a64-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

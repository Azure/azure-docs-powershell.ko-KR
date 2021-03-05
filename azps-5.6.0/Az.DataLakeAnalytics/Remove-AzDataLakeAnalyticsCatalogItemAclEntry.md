---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 968acf65d0f3e045614b5ade094bb50c90acac46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963136"
---
# <span data-ttu-id="b852e-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b852e-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="b852e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b852e-102">SYNOPSIS</span></span>
<span data-ttu-id="b852e-103">Data Lake Analytics의 카탈로그 또는 카탈로그 항목의 ACL에서 항목을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b852e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b852e-104">SYNTAX</span></span>

### <span data-ttu-id="b852e-105">RemoveCatalogAclEntryForUser(기본값)</span><span class="sxs-lookup"><span data-stu-id="b852e-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b852e-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="b852e-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b852e-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b852e-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b852e-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b852e-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b852e-109">설명</span><span class="sxs-lookup"><span data-stu-id="b852e-109">DESCRIPTION</span></span>
<span data-ttu-id="b852e-110">**Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet은 Data Lake Analytics의 카탈로그 또는 카탈로그 항목의 액세스 제어 목록(ACL)에서 ACE(항목)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b852e-111">예제</span><span class="sxs-lookup"><span data-stu-id="b852e-111">EXAMPLES</span></span>

### <span data-ttu-id="b852e-112">예제 1: 카탈로그에 대한 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="b852e-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="b852e-113">이 명령은 contosoadla 계정의 Patti Fuller에 대한 카탈로그 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="b852e-114">예제 2: 데이터베이스에 대한 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="b852e-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="b852e-115">이 명령은 contosoadla 계정의 Patti Fuller에 대한 데이터베이스 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="b852e-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b852e-116">PARAMETERS</span></span>

### <span data-ttu-id="b852e-117">-Account</span><span class="sxs-lookup"><span data-stu-id="b852e-117">-Account</span></span>
<span data-ttu-id="b852e-118">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b852e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b852e-119">-DefaultProfile</span></span>
<span data-ttu-id="b852e-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b852e-121">-Group</span><span class="sxs-lookup"><span data-stu-id="b852e-121">-Group</span></span>
<span data-ttu-id="b852e-122">그룹에 대한 카탈로그의 ACL 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b852e-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b852e-123">-ItemType</span></span>
<span data-ttu-id="b852e-124">카탈로그 또는 카탈로그 항목의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="b852e-125">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b852e-126">카탈로그</span><span class="sxs-lookup"><span data-stu-id="b852e-126">Catalog</span></span>
- <span data-ttu-id="b852e-127">데이터베이스</span><span class="sxs-lookup"><span data-stu-id="b852e-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b852e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b852e-128">-ObjectId</span></span>
<span data-ttu-id="b852e-129">제거할 사용자의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b852e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b852e-130">-PassThru</span></span>
<span data-ttu-id="b852e-131">삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="b852e-132">-Path</span><span class="sxs-lookup"><span data-stu-id="b852e-132">-Path</span></span>
<span data-ttu-id="b852e-133">카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="b852e-134">경로의 부분은 기간(.)으로 구분해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b852e-135">-User</span><span class="sxs-lookup"><span data-stu-id="b852e-135">-User</span></span>
<span data-ttu-id="b852e-136">사용자에 대한 카탈로그의 ACL 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b852e-137">-확인</span><span class="sxs-lookup"><span data-stu-id="b852e-137">-Confirm</span></span>
<span data-ttu-id="b852e-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b852e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b852e-139">-WhatIf</span></span>
<span data-ttu-id="b852e-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b852e-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b852e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b852e-142">CommonParameters</span></span>
<span data-ttu-id="b852e-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b852e-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b852e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b852e-145">입력</span><span class="sxs-lookup"><span data-stu-id="b852e-145">INPUTS</span></span>

### <span data-ttu-id="b852e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b852e-146">System.String</span></span>

### <span data-ttu-id="b852e-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b852e-147">System.Guid</span></span>

### <span data-ttu-id="b852e-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b852e-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="b852e-149">출력</span><span class="sxs-lookup"><span data-stu-id="b852e-149">OUTPUTS</span></span>

### <span data-ttu-id="b852e-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b852e-150">System.Boolean</span></span>

## <span data-ttu-id="b852e-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b852e-151">NOTES</span></span>

## <span data-ttu-id="b852e-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b852e-152">RELATED LINKS</span></span>

[<span data-ttu-id="b852e-153">U-SQL 이제 데이터베이스 수준 액세스 제어를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b852e-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="b852e-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b852e-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="b852e-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b852e-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

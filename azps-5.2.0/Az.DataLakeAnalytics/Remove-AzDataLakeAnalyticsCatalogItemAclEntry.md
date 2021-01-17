---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372877"
---
# <span data-ttu-id="6deba-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6deba-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="6deba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6deba-102">SYNOPSIS</span></span>
<span data-ttu-id="6deba-103">Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL에서 항목을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="6deba-104">구문</span><span class="sxs-lookup"><span data-stu-id="6deba-104">SYNTAX</span></span>

### <span data-ttu-id="6deba-105">RemoveCatalogAclEntryForUser(기본값)</span><span class="sxs-lookup"><span data-stu-id="6deba-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6deba-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="6deba-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6deba-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="6deba-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6deba-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="6deba-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6deba-109">설명</span><span class="sxs-lookup"><span data-stu-id="6deba-109">DESCRIPTION</span></span>
<span data-ttu-id="6deba-110">**Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet은 Data Lake Analytics의 카탈로그 또는 카탈로그 항목의 ACL(액세스 제어 목록)에서 ACE(항목)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="6deba-111">예제</span><span class="sxs-lookup"><span data-stu-id="6deba-111">EXAMPLES</span></span>

### <span data-ttu-id="6deba-112">예제 1: 카탈로그에 대한 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="6deba-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="6deba-113">이 명령은 contosoadla 계정의 Patti Fuller에 대한 카탈로그 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="6deba-114">예제 2: 데이터베이스에 대한 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="6deba-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="6deba-115">이 명령은 contosoadla 계정의 Patti Fuller에 대한 데이터베이스 ACL을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="6deba-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6deba-116">PARAMETERS</span></span>

### <span data-ttu-id="6deba-117">-Account</span><span class="sxs-lookup"><span data-stu-id="6deba-117">-Account</span></span>
<span data-ttu-id="6deba-118">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6deba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6deba-119">-DefaultProfile</span></span>
<span data-ttu-id="6deba-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6deba-121">-Group</span><span class="sxs-lookup"><span data-stu-id="6deba-121">-Group</span></span>
<span data-ttu-id="6deba-122">그룹에 대한 카탈로그의 ACL 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="6deba-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="6deba-123">-ItemType</span></span>
<span data-ttu-id="6deba-124">카탈로그 또는 카탈로그 항목의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="6deba-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="6deba-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6deba-126">카탈로그</span><span class="sxs-lookup"><span data-stu-id="6deba-126">Catalog</span></span>
- <span data-ttu-id="6deba-127">데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6deba-127">Database</span></span>

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

### <span data-ttu-id="6deba-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6deba-128">-ObjectId</span></span>
<span data-ttu-id="6deba-129">제거할 사용자의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="6deba-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6deba-130">-PassThru</span></span>
<span data-ttu-id="6deba-131">삭제 작업의 결과를 나타내는 부울 응답이 반환되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6deba-132">-Path</span><span class="sxs-lookup"><span data-stu-id="6deba-132">-Path</span></span>
<span data-ttu-id="6deba-133">카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="6deba-134">경로의 부분은 기간(.)으로 구분해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="6deba-135">-User</span><span class="sxs-lookup"><span data-stu-id="6deba-135">-User</span></span>
<span data-ttu-id="6deba-136">사용자에 대한 카탈로그의 ACL 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="6deba-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6deba-137">-Confirm</span></span>
<span data-ttu-id="6deba-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6deba-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6deba-139">-WhatIf</span></span>
<span data-ttu-id="6deba-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6deba-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6deba-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6deba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6deba-142">CommonParameters</span></span>
<span data-ttu-id="6deba-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6deba-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6deba-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6deba-145">입력</span><span class="sxs-lookup"><span data-stu-id="6deba-145">INPUTS</span></span>

### <span data-ttu-id="6deba-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6deba-146">System.String</span></span>

### <span data-ttu-id="6deba-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6deba-147">System.Guid</span></span>

### <span data-ttu-id="6deba-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="6deba-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="6deba-149">출력</span><span class="sxs-lookup"><span data-stu-id="6deba-149">OUTPUTS</span></span>

### <span data-ttu-id="6deba-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6deba-150">System.Boolean</span></span>

## <span data-ttu-id="6deba-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6deba-151">NOTES</span></span>

## <span data-ttu-id="6deba-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6deba-152">RELATED LINKS</span></span>

[<span data-ttu-id="6deba-153">이제 U-SQL 데이터베이스 수준 액세스 제어를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6deba-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="6deba-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6deba-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="6deba-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6deba-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e97876377e8ea96dc106277991bcc05fec5f3759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528541"
---
# <span data-ttu-id="0a645-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a645-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="0a645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a645-102">SYNOPSIS</span></span>
<span data-ttu-id="0a645-103">데이터 호수 분석에서 카탈로그 또는 카탈로그 항목의 ACL에서 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a645-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a645-104">SYNTAX</span></span>

### <span data-ttu-id="0a645-105">RemoveCatalogAclEntryForUser (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a645-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a645-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="0a645-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a645-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0a645-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a645-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0a645-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a645-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0a645-109">DESCRIPTION</span></span>
<span data-ttu-id="0a645-110">**AzureRmDataLakeAnalyticsCatalogItemAclEntry** Cmdlet은 Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL (액세스 제어 목록)에서 항목 (ACE)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-110">The **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0a645-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0a645-111">EXAMPLES</span></span>

### <span data-ttu-id="0a645-112">예제 1: 카탈로그에 대 한 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="0a645-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="0a645-113">이 명령은 contosoadla 계정 Patti의 카탈로그 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="0a645-114">예제 2: 데이터베이스의 사용자 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="0a645-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="0a645-115">이 명령은 contosoadla 계정 Patti의 데이터베이스 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="0a645-116">변수</span><span class="sxs-lookup"><span data-stu-id="0a645-116">PARAMETERS</span></span>

### <span data-ttu-id="0a645-117">-계정</span><span class="sxs-lookup"><span data-stu-id="0a645-117">-Account</span></span>
<span data-ttu-id="0a645-118">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0a645-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a645-119">-DefaultProfile</span></span>
<span data-ttu-id="0a645-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a645-121">-그룹</span><span class="sxs-lookup"><span data-stu-id="0a645-121">-Group</span></span>
<span data-ttu-id="0a645-122">그룹에 대 한 카탈로그의 ACL 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="0a645-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="0a645-123">-ItemType</span></span>
<span data-ttu-id="0a645-124">카탈로그 또는 카탈로그 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="0a645-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a645-126">카탈로그인</span><span class="sxs-lookup"><span data-stu-id="0a645-126">Catalog</span></span>
- <span data-ttu-id="0a645-127">데이터</span><span class="sxs-lookup"><span data-stu-id="0a645-127">Database</span></span>

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

### <span data-ttu-id="0a645-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0a645-128">-ObjectId</span></span>
<span data-ttu-id="0a645-129">제거할 사용자의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="0a645-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a645-130">-PassThru</span></span>
<span data-ttu-id="0a645-131">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0a645-132">-Path</span><span class="sxs-lookup"><span data-stu-id="0a645-132">-Path</span></span>
<span data-ttu-id="0a645-133">카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="0a645-134">경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="0a645-135">-사용자</span><span class="sxs-lookup"><span data-stu-id="0a645-135">-User</span></span>
<span data-ttu-id="0a645-136">사용자에 대 한 카탈로그의 ACL 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="0a645-137">-확인</span><span class="sxs-lookup"><span data-stu-id="0a645-137">-Confirm</span></span>
<span data-ttu-id="0a645-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a645-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a645-139">-WhatIf</span></span>
<span data-ttu-id="0a645-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a645-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a645-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a645-142">CommonParameters</span></span>
<span data-ttu-id="0a645-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a645-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a645-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a645-145">입력</span><span class="sxs-lookup"><span data-stu-id="0a645-145">INPUTS</span></span>

### <span data-ttu-id="0a645-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0a645-146">System.String</span></span>

### <span data-ttu-id="0a645-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="0a645-147">System.Guid</span></span>

### <span data-ttu-id="0a645-148">DataLakeAnalytics. CatalogPathInstance/.</span><span class="sxs-lookup"><span data-stu-id="0a645-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="0a645-149">출력</span><span class="sxs-lookup"><span data-stu-id="0a645-149">OUTPUTS</span></span>

### <span data-ttu-id="0a645-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0a645-150">System.Boolean</span></span>

## <span data-ttu-id="0a645-151">상속자</span><span class="sxs-lookup"><span data-stu-id="0a645-151">NOTES</span></span>

## <span data-ttu-id="0a645-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a645-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a645-153">U-SQL은 이제 데이터베이스 수준 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a645-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="0a645-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a645-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0a645-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a645-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
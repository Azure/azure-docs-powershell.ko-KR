---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305765"
---
# <span data-ttu-id="cfe12-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cfe12-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="cfe12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe12-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe12-103">Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL에 있는 항목을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="cfe12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cfe12-104">SYNTAX</span></span>

### <span data-ttu-id="cfe12-105">SetCatalogAclEntryForUser (기본값)</span><span class="sxs-lookup"><span data-stu-id="cfe12-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfe12-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="cfe12-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="cfe12-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfe12-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="cfe12-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="cfe12-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="cfe12-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe12-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe12-115">설명은</span><span class="sxs-lookup"><span data-stu-id="cfe12-115">DESCRIPTION</span></span>
<span data-ttu-id="cfe12-116">**AzDataLakeAnalyticsCatalogItemAclEntry** Cmdlet은 Data Lake Analytics에서 카탈로그 또는 카탈로그 항목의 ACL (액세스 제어 목록)에 항목 (ACE)을 추가 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="cfe12-117">예제의</span><span class="sxs-lookup"><span data-stu-id="cfe12-117">EXAMPLES</span></span>

### <span data-ttu-id="cfe12-118">예제 1: 카탈로그에 대 한 사용자 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="cfe12-119">이 명령은 Patti의 카탈로그 ACE를 수정 하 여 읽기 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="cfe12-120">예제 2: 데이터베이스에 대 한 사용자 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="cfe12-121">이 명령은 Patti의 데이터베이스 ACE를 수정 하 여 읽기 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="cfe12-122">예제 3: 카탈로그에 대 한 다른 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="cfe12-123">이 명령은 다른에 대 한 카탈로그 ACE를 수정 하도록 읽기 권한을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="cfe12-124">예제 4: 데이터베이스에 대 한 다른 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="cfe12-125">예제 5: 카탈로그에 대 한 사용자 소유자 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="cfe12-126">이 명령은 읽을 계정에 대 한 소유자 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="cfe12-127">예제 6: 데이터베이스에 대 한 사용자 소유자 권한 수정</span><span class="sxs-lookup"><span data-stu-id="cfe12-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="cfe12-128">이 명령은 데이터베이스의 소유자 권한을 읽을 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="cfe12-129">변수</span><span class="sxs-lookup"><span data-stu-id="cfe12-129">PARAMETERS</span></span>

### <span data-ttu-id="cfe12-130">-계정</span><span class="sxs-lookup"><span data-stu-id="cfe12-130">-Account</span></span>
<span data-ttu-id="cfe12-131">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cfe12-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe12-132">-DefaultProfile</span></span>
<span data-ttu-id="cfe12-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe12-134">-그룹</span><span class="sxs-lookup"><span data-stu-id="cfe12-134">-Group</span></span>
<span data-ttu-id="cfe12-135">그룹에 대 한 카탈로그의 ACL 항목을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-136">-GroupOwner</span></span>
<span data-ttu-id="cfe12-137">그룹 소유자에 대 한 카탈로그의 ACL 항목을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="cfe12-138">-ItemType</span></span>
<span data-ttu-id="cfe12-139">카탈로그 또는 카탈로그 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="cfe12-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfe12-141">카탈로그인</span><span class="sxs-lookup"><span data-stu-id="cfe12-141">Catalog</span></span>
- <span data-ttu-id="cfe12-142">데이터</span><span class="sxs-lookup"><span data-stu-id="cfe12-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cfe12-143">-ObjectId</span></span>
<span data-ttu-id="cfe12-144">설정할 사용자의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-145">-다른</span><span class="sxs-lookup"><span data-stu-id="cfe12-145">-Other</span></span>
<span data-ttu-id="cfe12-146">다른 카탈로그의 ACL 항목을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-147">-Path</span><span class="sxs-lookup"><span data-stu-id="cfe12-147">-Path</span></span>
<span data-ttu-id="cfe12-148">카탈로그 또는 카탈로그 항목의 Data Lake Analytics 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="cfe12-149">경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-150">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="cfe12-150">-Permissions</span></span>
<span data-ttu-id="cfe12-151">ACE에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="cfe12-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfe12-153">않아야</span><span class="sxs-lookup"><span data-stu-id="cfe12-153">None</span></span>
- <span data-ttu-id="cfe12-154">자세한</span><span class="sxs-lookup"><span data-stu-id="cfe12-154">Read</span></span>
- <span data-ttu-id="cfe12-155">쓰기</span><span class="sxs-lookup"><span data-stu-id="cfe12-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-156">-사용자</span><span class="sxs-lookup"><span data-stu-id="cfe12-156">-User</span></span>
<span data-ttu-id="cfe12-157">사용자에 대 한 카탈로그의 ACL 항목을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="cfe12-158">-UserOwner</span></span>
<span data-ttu-id="cfe12-159">사용자 소유자에 대 한 카탈로그의 ACL 항목을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe12-160">-확인</span><span class="sxs-lookup"><span data-stu-id="cfe12-160">-Confirm</span></span>
<span data-ttu-id="cfe12-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe12-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe12-162">-WhatIf</span></span>
<span data-ttu-id="cfe12-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe12-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe12-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe12-165">CommonParameters</span></span>
<span data-ttu-id="cfe12-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe12-167">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe12-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe12-168">입력</span><span class="sxs-lookup"><span data-stu-id="cfe12-168">INPUTS</span></span>

### <span data-ttu-id="cfe12-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cfe12-169">System.String</span></span>

### <span data-ttu-id="cfe12-170">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="cfe12-170">System.Guid</span></span>

### <span data-ttu-id="cfe12-171">DataLakeAnalytics. CatalogPathInstance/.</span><span class="sxs-lookup"><span data-stu-id="cfe12-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="cfe12-172">DataLakeAnalytics. DataLakeAnalyticsEnums + 고 대 형식</span><span class="sxs-lookup"><span data-stu-id="cfe12-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="cfe12-173">출력</span><span class="sxs-lookup"><span data-stu-id="cfe12-173">OUTPUTS</span></span>

### <span data-ttu-id="cfe12-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="cfe12-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="cfe12-175">상속자</span><span class="sxs-lookup"><span data-stu-id="cfe12-175">NOTES</span></span>

## <span data-ttu-id="cfe12-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfe12-176">RELATED LINKS</span></span>

[<span data-ttu-id="cfe12-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cfe12-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="cfe12-178">제거-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cfe12-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="cfe12-179">U-SQL은 이제 데이터베이스 수준 액세스 제어를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfe12-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

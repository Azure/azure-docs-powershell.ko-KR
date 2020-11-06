---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526831"
---
# <span data-ttu-id="9779d-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9779d-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="9779d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9779d-102">SYNOPSIS</span></span>
<span data-ttu-id="9779d-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9779d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9779d-104">SYNTAX</span></span>

### <span data-ttu-id="9779d-105">Setbyac(기본값)</span><span class="sxs-lookup"><span data-stu-id="9779d-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9779d-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="9779d-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9779d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9779d-107">DESCRIPTION</span></span>
<span data-ttu-id="9779d-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)에 있는 항목 (ACE)을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9779d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9779d-109">EXAMPLES</span></span>

### <span data-ttu-id="9779d-110">예제 1: ACE에 대 한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="9779d-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="9779d-111">이 명령은 Patti의 ACE를 수정 하 여 모든 권한을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="9779d-112">변수</span><span class="sxs-lookup"><span data-stu-id="9779d-112">PARAMETERS</span></span>

### <span data-ttu-id="9779d-113">-계정</span><span class="sxs-lookup"><span data-stu-id="9779d-113">-Account</span></span>
<span data-ttu-id="9779d-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="9779d-115">-AceType</span></span>
<span data-ttu-id="9779d-116">수정할 ACE 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="9779d-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9779d-118">클릭할</span><span class="sxs-lookup"><span data-stu-id="9779d-118">User</span></span> 
- <span data-ttu-id="9779d-119">그룹과</span><span class="sxs-lookup"><span data-stu-id="9779d-119">Group</span></span> 
- <span data-ttu-id="9779d-120">마스킹하</span><span class="sxs-lookup"><span data-stu-id="9779d-120">Mask</span></span> 
- <span data-ttu-id="9779d-121">나머지</span><span class="sxs-lookup"><span data-stu-id="9779d-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-122">-Acl</span><span class="sxs-lookup"><span data-stu-id="9779d-122">-Acl</span></span>
<span data-ttu-id="9779d-123">수정할 항목이 포함 된 ACL 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-124">-기본</span><span class="sxs-lookup"><span data-stu-id="9779d-124">-Default</span></span>
<span data-ttu-id="9779d-125">이 작업을 수행 하면 지정 된 ACL의 기본 ACE가 수정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9779d-126">-DefaultProfile</span></span>
<span data-ttu-id="9779d-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9779d-128">-Id</span><span class="sxs-lookup"><span data-stu-id="9779d-128">-Id</span></span>
<span data-ttu-id="9779d-129">ACE를 수정할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9779d-130">-PassThru</span></span>
<span data-ttu-id="9779d-131">결과 ACL을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-132">-Path</span><span class="sxs-lookup"><span data-stu-id="9779d-132">-Path</span></span>
<span data-ttu-id="9779d-133">ACE를 수정할 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-134">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="9779d-134">-Permissions</span></span>
<span data-ttu-id="9779d-135">ACE에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="9779d-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9779d-137">않아야</span><span class="sxs-lookup"><span data-stu-id="9779d-137">None</span></span>
- <span data-ttu-id="9779d-138">세기</span><span class="sxs-lookup"><span data-stu-id="9779d-138">Execute</span></span>
- <span data-ttu-id="9779d-139">작성</span><span class="sxs-lookup"><span data-stu-id="9779d-139">Write</span></span>
- <span data-ttu-id="9779d-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="9779d-140">WriteExecute</span></span>
- <span data-ttu-id="9779d-141">자세한</span><span class="sxs-lookup"><span data-stu-id="9779d-141">Read</span></span>
- <span data-ttu-id="9779d-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="9779d-142">ReadExecute</span></span>
- <span data-ttu-id="9779d-143">쓰기</span><span class="sxs-lookup"><span data-stu-id="9779d-143">ReadWrite</span></span>
- <span data-ttu-id="9779d-144">모든</span><span class="sxs-lookup"><span data-stu-id="9779d-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9779d-145">-확인</span><span class="sxs-lookup"><span data-stu-id="9779d-145">-Confirm</span></span>
<span data-ttu-id="9779d-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9779d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9779d-147">-WhatIf</span></span>
<span data-ttu-id="9779d-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9779d-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9779d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9779d-150">CommonParameters</span></span>
<span data-ttu-id="9779d-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9779d-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9779d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9779d-153">입력</span><span class="sxs-lookup"><span data-stu-id="9779d-153">INPUTS</span></span>

### <span data-ttu-id="9779d-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="9779d-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="9779d-155">' Acl ' 매개 변수는 파이프라인에서 ' DataLakeStoreItemAce [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="9779d-156">출력</span><span class="sxs-lookup"><span data-stu-id="9779d-156">OUTPUTS</span></span>

### <span data-ttu-id="9779d-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="9779d-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="9779d-158">PassThru를 지정 하면 ACL 엔트리의 결과 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9779d-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="9779d-159">상속자</span><span class="sxs-lookup"><span data-stu-id="9779d-159">NOTES</span></span>

## <span data-ttu-id="9779d-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9779d-160">RELATED LINKS</span></span>

[<span data-ttu-id="9779d-161">제거-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9779d-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)



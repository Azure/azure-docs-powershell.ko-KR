---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703743"
---
# <span data-ttu-id="f92e7-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f92e7-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f92e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f92e7-103">Data Lake Store의 파일 또는 폴더의 ACL에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f92e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f92e7-104">SYNTAX</span></span>

### <span data-ttu-id="f92e7-105">ACL 개체를 사용 하 여 ACL 항목 제거 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f92e7-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f92e7-106">특정 ACE 제거</span><span class="sxs-lookup"><span data-stu-id="f92e7-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f92e7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f92e7-107">DESCRIPTION</span></span>
<span data-ttu-id="f92e7-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에 있는 파일 또는 폴더의 ACL (액세스 제어 목록)에서 항목 (ACE)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f92e7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f92e7-109">EXAMPLES</span></span>

### <span data-ttu-id="f92e7-110">예제 1: 사용자 항목 제거</span><span class="sxs-lookup"><span data-stu-id="f92e7-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="f92e7-111">이 명령은 ContosoADL 계정에서 Patti의 사용자 ACE를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="f92e7-112">변수</span><span class="sxs-lookup"><span data-stu-id="f92e7-112">PARAMETERS</span></span>

### <span data-ttu-id="f92e7-113">-계정</span><span class="sxs-lookup"><span data-stu-id="f92e7-113">-Account</span></span>
<span data-ttu-id="f92e7-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f92e7-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="f92e7-115">-AceType</span></span>
<span data-ttu-id="f92e7-116">제거할 ACE 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="f92e7-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f92e7-118">클릭할</span><span class="sxs-lookup"><span data-stu-id="f92e7-118">User</span></span>
- <span data-ttu-id="f92e7-119">그룹과</span><span class="sxs-lookup"><span data-stu-id="f92e7-119">Group</span></span>
- <span data-ttu-id="f92e7-120">마스킹하</span><span class="sxs-lookup"><span data-stu-id="f92e7-120">Mask</span></span>
- <span data-ttu-id="f92e7-121">나머지</span><span class="sxs-lookup"><span data-stu-id="f92e7-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-122">-Acl</span><span class="sxs-lookup"><span data-stu-id="f92e7-122">-Acl</span></span>
<span data-ttu-id="f92e7-123">제거할 항목이 포함 된 ACL 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-124">-기본</span><span class="sxs-lookup"><span data-stu-id="f92e7-124">-Default</span></span>
<span data-ttu-id="f92e7-125">이 작업을 수행 하면 지정 된 ACL에서 기본 ACE가 제거 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-126">-Id</span><span class="sxs-lookup"><span data-stu-id="f92e7-126">-Id</span></span>
<span data-ttu-id="f92e7-127">ACE를 제거할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f92e7-128">-PassThru</span></span>
<span data-ttu-id="f92e7-129">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f92e7-130">-Path</span></span>
<span data-ttu-id="f92e7-131">ACE를 제거할 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92e7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="f92e7-132">-Confirm</span></span>
<span data-ttu-id="f92e7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f92e7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92e7-134">-WhatIf</span></span>
<span data-ttu-id="f92e7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f92e7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f92e7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92e7-137">-DefaultProfile</span></span>
<span data-ttu-id="f92e7-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f92e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92e7-139">CommonParameters</span></span>
<span data-ttu-id="f92e7-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92e7-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f92e7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92e7-142">입력</span><span class="sxs-lookup"><span data-stu-id="f92e7-142">INPUTS</span></span>

### <span data-ttu-id="f92e7-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="f92e7-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="f92e7-144">' Acl ' 매개 변수는 파이프라인에서 ' DataLakeStoreItemAce [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="f92e7-145">출력</span><span class="sxs-lookup"><span data-stu-id="f92e7-145">OUTPUTS</span></span>

### <span data-ttu-id="f92e7-146">부울</span><span class="sxs-lookup"><span data-stu-id="f92e7-146">bool</span></span>
<span data-ttu-id="f92e7-147">PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f92e7-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="f92e7-148">상속자</span><span class="sxs-lookup"><span data-stu-id="f92e7-148">NOTES</span></span>

## <span data-ttu-id="f92e7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f92e7-149">RELATED LINKS</span></span>

[<span data-ttu-id="f92e7-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f92e7-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344277"
---
# <span data-ttu-id="a7b09-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7b09-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="a7b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b09-103">Azure Data Lake에서 삭제된 파일 또는 폴더를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="a7b09-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7b09-104">SYNTAX</span></span>

### <span data-ttu-id="a7b09-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7b09-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b09-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7b09-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7b09-107">설명</span><span class="sxs-lookup"><span data-stu-id="a7b09-107">DESCRIPTION</span></span>
<span data-ttu-id="a7b09-108">**Restore-AzDataLakeStoreDeletedItem** cmdlet은 Data Lake Store에서 삭제된 파일 또는 폴더를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="a7b09-109">Get-AzDataLakeStoreDeletedItem에서 반환된 휴지통에서 삭제된 항목의 경로가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="a7b09-110">주의: 파일을 삭제하지 않는 것이 가장 좋은 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="a7b09-111">파일을 삭제한 후 복원할 수 있는 보장은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="a7b09-112">이 API는 화이트리스트를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="a7b09-113">ADL 계정이 화이트리스트에 없는 경우 이 API를 사용하여 구현되지 않은 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="a7b09-114">자세한 정보 및 지원은 Microsoft 지원에 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="a7b09-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="a7b09-115">예제</span><span class="sxs-lookup"><span data-stu-id="a7b09-115">EXAMPLES</span></span>

### <span data-ttu-id="a7b09-116">예제 1: -force 옵션을 사용하여 Data Lake Store에서 파일 복원</span><span class="sxs-lookup"><span data-stu-id="a7b09-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="a7b09-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b09-117">PARAMETERS</span></span>

### <span data-ttu-id="a7b09-118">-Account</span><span class="sxs-lookup"><span data-stu-id="a7b09-118">-Account</span></span>
<span data-ttu-id="a7b09-119">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a7b09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b09-120">-DefaultProfile</span></span>
<span data-ttu-id="a7b09-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b09-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7b09-122">-DeletedItem</span></span>
<span data-ttu-id="a7b09-123">삭제된 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-123">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b09-124">-Destination</span><span class="sxs-lookup"><span data-stu-id="a7b09-124">-Destination</span></span>
<span data-ttu-id="a7b09-125">삭제된 파일 또는 폴더를 복원해야 하는 대상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-125">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b09-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a7b09-126">-Force</span></span>
<span data-ttu-id="a7b09-127">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7b09-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7b09-128">-PassThru</span></span>
<span data-ttu-id="a7b09-129">성공 시 부울 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="a7b09-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a7b09-130">-Path</span></span>
<span data-ttu-id="a7b09-131">삭제된 파일 또는 휴지통에 있는 폴더의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-131">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b09-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="a7b09-132">-RestoreAction</span></span>
<span data-ttu-id="a7b09-133">대상 이름 충돌에 대한 작업 - "복사" 또는 "덮어 사용"</span><span class="sxs-lookup"><span data-stu-id="a7b09-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b09-134">-Type</span><span class="sxs-lookup"><span data-stu-id="a7b09-134">-Type</span></span>
<span data-ttu-id="a7b09-135">복원할 항목의 유형 - "파일" 또는 "폴더"</span><span class="sxs-lookup"><span data-stu-id="a7b09-135">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b09-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b09-136">CommonParameters</span></span>
<span data-ttu-id="a7b09-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b09-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b09-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a7b09-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b09-139">입력</span><span class="sxs-lookup"><span data-stu-id="a7b09-139">INPUTS</span></span>

### <span data-ttu-id="a7b09-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a7b09-140">System.String</span></span>

## <span data-ttu-id="a7b09-141">출력</span><span class="sxs-lookup"><span data-stu-id="a7b09-141">OUTPUTS</span></span>

### <span data-ttu-id="a7b09-142">없음</span><span class="sxs-lookup"><span data-stu-id="a7b09-142">None</span></span>

## <span data-ttu-id="a7b09-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7b09-143">NOTES</span></span>

## <span data-ttu-id="a7b09-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7b09-144">RELATED LINKS</span></span>

[<span data-ttu-id="a7b09-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7b09-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)
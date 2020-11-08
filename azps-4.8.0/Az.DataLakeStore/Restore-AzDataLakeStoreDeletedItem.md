---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056410"
---
# <span data-ttu-id="102b5-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="102b5-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="102b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="102b5-102">SYNOPSIS</span></span>
<span data-ttu-id="102b5-103">Azure Data Lake에서 삭제 된 파일 또는 폴더를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="102b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="102b5-104">SYNTAX</span></span>

### <span data-ttu-id="102b5-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="102b5-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="102b5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="102b5-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="102b5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="102b5-107">DESCRIPTION</span></span>
<span data-ttu-id="102b5-108">**Restore-AzDataLakeStoreDeletedItem** Cmdlet은 Data Lake store에서 삭제 된 파일 또는 폴더를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="102b5-109">AzDataLakeStoreDeletedItem에서 반환 된 휴지통의 삭제 된 항목 경로가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="102b5-110">주의: Undeleting 파일은 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="102b5-111">삭제 된 파일은 복원할 수 없다는 보장이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="102b5-112">이 API의 사용은 whitelisting를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="102b5-113">ADL 계정이 허용 목록이 아닌 경우이 api를 사용 하면 구현 되지 않은 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="102b5-114">자세한 정보 및 지원은 Microsoft 지원에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="102b5-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="102b5-115">예제의</span><span class="sxs-lookup"><span data-stu-id="102b5-115">EXAMPLES</span></span>

### <span data-ttu-id="102b5-116">예제 1:-force 옵션을 사용 하 여 Data Lake Store에서 파일 복원</span><span class="sxs-lookup"><span data-stu-id="102b5-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="102b5-117">변수</span><span class="sxs-lookup"><span data-stu-id="102b5-117">PARAMETERS</span></span>

### <span data-ttu-id="102b5-118">-계정</span><span class="sxs-lookup"><span data-stu-id="102b5-118">-Account</span></span>
<span data-ttu-id="102b5-119">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="102b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102b5-120">-DefaultProfile</span></span>
<span data-ttu-id="102b5-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102b5-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="102b5-122">-DeletedItem</span></span>
<span data-ttu-id="102b5-123">삭제 된 항목 개체</span><span class="sxs-lookup"><span data-stu-id="102b5-123">The deleted item object.</span></span>

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

### <span data-ttu-id="102b5-124">-대상</span><span class="sxs-lookup"><span data-stu-id="102b5-124">-Destination</span></span>
<span data-ttu-id="102b5-125">삭제 된 파일 또는 폴더를 복원할 대상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="102b5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="102b5-126">-Force</span></span>
<span data-ttu-id="102b5-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="102b5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="102b5-128">-PassThru</span></span>
<span data-ttu-id="102b5-129">성공에 부울 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="102b5-130">-Path</span><span class="sxs-lookup"><span data-stu-id="102b5-130">-Path</span></span>
<span data-ttu-id="102b5-131">휴지통에서 삭제 된 파일 또는 폴더의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="102b5-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="102b5-132">-RestoreAction</span></span>
<span data-ttu-id="102b5-133">대상 이름 충돌 시 수행할 작업-"copy" 또는 "overwrite"</span><span class="sxs-lookup"><span data-stu-id="102b5-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="102b5-134">-Type</span><span class="sxs-lookup"><span data-stu-id="102b5-134">-Type</span></span>
<span data-ttu-id="102b5-135">복원할 항목 유형-"file" 또는 "folder"</span><span class="sxs-lookup"><span data-stu-id="102b5-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="102b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102b5-136">CommonParameters</span></span>
<span data-ttu-id="102b5-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="102b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102b5-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="102b5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102b5-139">입력</span><span class="sxs-lookup"><span data-stu-id="102b5-139">INPUTS</span></span>

### <span data-ttu-id="102b5-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="102b5-140">System.String</span></span>

## <span data-ttu-id="102b5-141">출력</span><span class="sxs-lookup"><span data-stu-id="102b5-141">OUTPUTS</span></span>

### <span data-ttu-id="102b5-142">않아야</span><span class="sxs-lookup"><span data-stu-id="102b5-142">None</span></span>

## <span data-ttu-id="102b5-143">상속자</span><span class="sxs-lookup"><span data-stu-id="102b5-143">NOTES</span></span>

## <span data-ttu-id="102b5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="102b5-144">RELATED LINKS</span></span>

[<span data-ttu-id="102b5-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="102b5-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696809"
---
# <span data-ttu-id="44c84-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="44c84-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="44c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c84-102">SYNOPSIS</span></span>
<span data-ttu-id="44c84-103">Azure Data Lake에서 삭제 된 파일 또는 폴더를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="44c84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44c84-104">SYNTAX</span></span>

### <span data-ttu-id="44c84-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="44c84-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44c84-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="44c84-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44c84-107">설명은</span><span class="sxs-lookup"><span data-stu-id="44c84-107">DESCRIPTION</span></span>
<span data-ttu-id="44c84-108">**Restore-AzDataLakeStoreDeletedItem** Cmdlet은 Data Lake store에서 삭제 된 파일 또는 폴더를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="44c84-109">AzDataLakeStoreDeletedItem에서 반환 된 휴지통의 삭제 된 항목 경로가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="44c84-110">예제의</span><span class="sxs-lookup"><span data-stu-id="44c84-110">EXAMPLES</span></span>

### <span data-ttu-id="44c84-111">예제 1:-force 옵션을 사용 하 여 Data Lake Store에서 파일 복원</span><span class="sxs-lookup"><span data-stu-id="44c84-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="44c84-112">변수</span><span class="sxs-lookup"><span data-stu-id="44c84-112">PARAMETERS</span></span>

### <span data-ttu-id="44c84-113">-계정</span><span class="sxs-lookup"><span data-stu-id="44c84-113">-Account</span></span>
<span data-ttu-id="44c84-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="44c84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c84-115">-DefaultProfile</span></span>
<span data-ttu-id="44c84-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c84-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="44c84-117">-DeletedItem</span></span>
<span data-ttu-id="44c84-118">삭제 된 항목 개체</span><span class="sxs-lookup"><span data-stu-id="44c84-118">The deleted item object.</span></span>

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

### <span data-ttu-id="44c84-119">-대상</span><span class="sxs-lookup"><span data-stu-id="44c84-119">-Destination</span></span>
<span data-ttu-id="44c84-120">삭제 된 파일 또는 폴더를 복원할 대상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-120">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="44c84-121">-Force</span><span class="sxs-lookup"><span data-stu-id="44c84-121">-Force</span></span>
<span data-ttu-id="44c84-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44c84-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44c84-123">-PassThru</span></span>
<span data-ttu-id="44c84-124">성공에 부울 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="44c84-125">-Path</span><span class="sxs-lookup"><span data-stu-id="44c84-125">-Path</span></span>
<span data-ttu-id="44c84-126">휴지통에서 삭제 된 파일 또는 폴더의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-126">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="44c84-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="44c84-127">-RestoreAction</span></span>
<span data-ttu-id="44c84-128">대상 이름 충돌 시 수행할 작업-"copy" 또는 "overwrite"</span><span class="sxs-lookup"><span data-stu-id="44c84-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="44c84-129">-Type</span><span class="sxs-lookup"><span data-stu-id="44c84-129">-Type</span></span>
<span data-ttu-id="44c84-130">복원할 항목 유형-"file" 또는 "folder"</span><span class="sxs-lookup"><span data-stu-id="44c84-130">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="44c84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c84-131">CommonParameters</span></span>
<span data-ttu-id="44c84-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c84-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c84-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c84-134">입력</span><span class="sxs-lookup"><span data-stu-id="44c84-134">INPUTS</span></span>

### <span data-ttu-id="44c84-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44c84-135">System.String</span></span>

## <span data-ttu-id="44c84-136">출력</span><span class="sxs-lookup"><span data-stu-id="44c84-136">OUTPUTS</span></span>

### <span data-ttu-id="44c84-137">않아야</span><span class="sxs-lookup"><span data-stu-id="44c84-137">None</span></span>

## <span data-ttu-id="44c84-138">상속자</span><span class="sxs-lookup"><span data-stu-id="44c84-138">NOTES</span></span>

## <span data-ttu-id="44c84-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44c84-139">RELATED LINKS</span></span>

[<span data-ttu-id="44c84-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="44c84-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)
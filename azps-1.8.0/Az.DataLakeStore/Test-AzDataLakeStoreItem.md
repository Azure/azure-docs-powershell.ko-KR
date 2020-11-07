---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701044"
---
# <span data-ttu-id="d2a58-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d2a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a58-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a58-103">Data Lake Store에서 파일 또는 폴더가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d2a58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2a58-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2a58-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a58-106">**AzDataLakeStoreItem** Cmdlet은 Data Lake store에 파일 또는 폴더가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d2a58-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d2a58-107">EXAMPLES</span></span>

### <span data-ttu-id="d2a58-108">예제 1: 파일 테스트</span><span class="sxs-lookup"><span data-stu-id="d2a58-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="d2a58-109">이 명령은 ContosoADL 계정에 파일 Test.csv 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="d2a58-110">변수</span><span class="sxs-lookup"><span data-stu-id="d2a58-110">PARAMETERS</span></span>

### <span data-ttu-id="d2a58-111">-계정</span><span class="sxs-lookup"><span data-stu-id="d2a58-111">-Account</span></span>
<span data-ttu-id="d2a58-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d2a58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a58-113">-DefaultProfile</span></span>
<span data-ttu-id="d2a58-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a58-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d2a58-115">-Path</span></span>
<span data-ttu-id="d2a58-116">루트 디렉터리 (/)로 시작 하 여 테스트할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d2a58-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="d2a58-117">-PathType</span></span>
<span data-ttu-id="d2a58-118">테스트할 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="d2a58-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2a58-120">이상</span><span class="sxs-lookup"><span data-stu-id="d2a58-120">Any</span></span> 
- <span data-ttu-id="d2a58-121">파일</span><span class="sxs-lookup"><span data-stu-id="d2a58-121">File</span></span> 
- <span data-ttu-id="d2a58-122">폴더</span><span class="sxs-lookup"><span data-stu-id="d2a58-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a58-123">CommonParameters</span></span>
<span data-ttu-id="d2a58-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a58-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a58-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a58-126">입력</span><span class="sxs-lookup"><span data-stu-id="d2a58-126">INPUTS</span></span>

### <span data-ttu-id="d2a58-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2a58-127">System.String</span></span>

### <span data-ttu-id="d2a58-128">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="d2a58-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d2a58-129">DataLakeStore/DataLakeStoreEnums + PathType (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2a58-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="d2a58-130">출력</span><span class="sxs-lookup"><span data-stu-id="d2a58-130">OUTPUTS</span></span>

### <span data-ttu-id="d2a58-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d2a58-131">System.Boolean</span></span>

## <span data-ttu-id="d2a58-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d2a58-132">NOTES</span></span>

## <span data-ttu-id="d2a58-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2a58-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2a58-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d2a58-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d2a58-136">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d2a58-137">참가-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="d2a58-138">이동-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="d2a58-139">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d2a58-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)



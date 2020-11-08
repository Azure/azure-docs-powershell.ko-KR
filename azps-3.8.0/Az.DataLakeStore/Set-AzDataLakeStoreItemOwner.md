---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045025"
---
# <span data-ttu-id="9c95b-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9c95b-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="9c95b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c95b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c95b-103">Data Lake Store에서 파일 또는 폴더의 소유자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9c95b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c95b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c95b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c95b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c95b-106">**AzDataLakeStoreItemOwner** Cmdlet은 Data Lake store에서 파일 또는 폴더의 소유자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9c95b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c95b-107">EXAMPLES</span></span>

### <span data-ttu-id="9c95b-108">예제 1: 항목의 소유자 설정</span><span class="sxs-lookup"><span data-stu-id="9c95b-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="9c95b-109">이 명령은 루트 디렉터리의 소유자를 Patti로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="9c95b-110">변수</span><span class="sxs-lookup"><span data-stu-id="9c95b-110">PARAMETERS</span></span>

### <span data-ttu-id="9c95b-111">-계정</span><span class="sxs-lookup"><span data-stu-id="9c95b-111">-Account</span></span>
<span data-ttu-id="9c95b-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9c95b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c95b-113">-DefaultProfile</span></span>
<span data-ttu-id="9c95b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c95b-115">-Id</span><span class="sxs-lookup"><span data-stu-id="9c95b-115">-Id</span></span>
<span data-ttu-id="9c95b-116">소유자로 사용할 AzureActive Directory 사용자, 그룹 또는 서비스 사용자의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c95b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c95b-117">-PassThru</span></span>
<span data-ttu-id="9c95b-118">업데이트 된 소유자 결과를 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="9c95b-119">-Path</span><span class="sxs-lookup"><span data-stu-id="9c95b-119">-Path</span></span>
<span data-ttu-id="9c95b-120">루트 디렉터리 (/)로 시작 하 여 수정할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9c95b-121">-Type</span><span class="sxs-lookup"><span data-stu-id="9c95b-121">-Type</span></span>
<span data-ttu-id="9c95b-122">설정할 소유자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="9c95b-123">이 매개 변수에 허용 되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c95b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="9c95b-124">-Confirm</span></span>
<span data-ttu-id="9c95b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c95b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c95b-126">-WhatIf</span></span>
<span data-ttu-id="9c95b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c95b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c95b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c95b-129">CommonParameters</span></span>
<span data-ttu-id="9c95b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c95b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c95b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c95b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c95b-132">입력</span><span class="sxs-lookup"><span data-stu-id="9c95b-132">INPUTS</span></span>

### <span data-ttu-id="9c95b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c95b-133">System.String</span></span>

### <span data-ttu-id="9c95b-134">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="9c95b-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9c95b-135">DataLakeStore DataLakeStoreEnums + Owner (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9c95b-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="9c95b-136">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="9c95b-136">System.Guid</span></span>

### <span data-ttu-id="9c95b-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c95b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c95b-138">출력</span><span class="sxs-lookup"><span data-stu-id="9c95b-138">OUTPUTS</span></span>

### <span data-ttu-id="9c95b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c95b-139">System.String</span></span>

## <span data-ttu-id="9c95b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9c95b-140">NOTES</span></span>

## <span data-ttu-id="9c95b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c95b-141">RELATED LINKS</span></span>

[<span data-ttu-id="9c95b-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9c95b-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)



---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711899"
---
# <span data-ttu-id="092ee-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="092ee-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="092ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="092ee-102">SYNOPSIS</span></span>
<span data-ttu-id="092ee-103">Data Lake Store에서 파일 또는 폴더의 소유자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="092ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="092ee-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="092ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="092ee-105">DESCRIPTION</span></span>
<span data-ttu-id="092ee-106">**AzureRmDataLakeStoreItemOwner** Cmdlet은 Data Lake store에서 파일 또는 폴더의 소유자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="092ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="092ee-107">EXAMPLES</span></span>

### <span data-ttu-id="092ee-108">예제 1: 항목의 소유자 설정</span><span class="sxs-lookup"><span data-stu-id="092ee-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="092ee-109">이 명령은 루트 디렉터리의 소유자를 Patti로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="092ee-110">변수</span><span class="sxs-lookup"><span data-stu-id="092ee-110">PARAMETERS</span></span>

### <span data-ttu-id="092ee-111">-계정</span><span class="sxs-lookup"><span data-stu-id="092ee-111">-Account</span></span>
<span data-ttu-id="092ee-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="092ee-113">-Id</span><span class="sxs-lookup"><span data-stu-id="092ee-113">-Id</span></span>
<span data-ttu-id="092ee-114">소유자로 사용할 AzureActive Directory 사용자, 그룹 또는 서비스 사용자의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="092ee-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="092ee-115">-PassThru</span></span>
<span data-ttu-id="092ee-116">업데이트 된 소유자 결과를 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-116">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="092ee-117">-Path</span><span class="sxs-lookup"><span data-stu-id="092ee-117">-Path</span></span>
<span data-ttu-id="092ee-118">루트 디렉터리 (/)로 시작 하 여 수정할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="092ee-119">-Type</span><span class="sxs-lookup"><span data-stu-id="092ee-119">-Type</span></span>
<span data-ttu-id="092ee-120">설정할 소유자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="092ee-121">이 매개 변수에 허용 되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-121">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="092ee-122">-확인</span><span class="sxs-lookup"><span data-stu-id="092ee-122">-Confirm</span></span>
<span data-ttu-id="092ee-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="092ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="092ee-124">-WhatIf</span></span>
<span data-ttu-id="092ee-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="092ee-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="092ee-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092ee-127">-DefaultProfile</span></span>
<span data-ttu-id="092ee-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="092ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092ee-129">CommonParameters</span></span>
<span data-ttu-id="092ee-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092ee-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="092ee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092ee-132">입력</span><span class="sxs-lookup"><span data-stu-id="092ee-132">INPUTS</span></span>

## <span data-ttu-id="092ee-133">출력</span><span class="sxs-lookup"><span data-stu-id="092ee-133">OUTPUTS</span></span>

### <span data-ttu-id="092ee-134">이름</span><span class="sxs-lookup"><span data-stu-id="092ee-134">string</span></span>
<span data-ttu-id="092ee-135">PassThru가 지정 된 경우 업데이트 된 소유자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="092ee-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="092ee-136">상속자</span><span class="sxs-lookup"><span data-stu-id="092ee-136">NOTES</span></span>

## <span data-ttu-id="092ee-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="092ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="092ee-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="092ee-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)



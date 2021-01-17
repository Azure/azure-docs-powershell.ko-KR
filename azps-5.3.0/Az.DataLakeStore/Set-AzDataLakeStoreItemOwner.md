---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489055"
---
# <span data-ttu-id="4f0e1-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="4f0e1-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="4f0e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0e1-103">Data Lake Store에서 파일 또는 폴더의 소유자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4f0e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f0e1-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f0e1-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="4f0e1-106">**Set-AzDataLakeStoreItemOwner** cmdlet은 Data Lake Store에서 파일 또는 폴더의 소유자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4f0e1-107">예제</span><span class="sxs-lookup"><span data-stu-id="4f0e1-107">EXAMPLES</span></span>

### <span data-ttu-id="4f0e1-108">예제 1: 항목에 대한 소유자 설정</span><span class="sxs-lookup"><span data-stu-id="4f0e1-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="4f0e1-109">이 명령은 루트 디렉터리의 소유자를 Patti Fuller로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="4f0e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f0e1-110">PARAMETERS</span></span>

### <span data-ttu-id="4f0e1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4f0e1-111">-Account</span></span>
<span data-ttu-id="4f0e1-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4f0e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0e1-113">-DefaultProfile</span></span>
<span data-ttu-id="4f0e1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f0e1-115">-Id</span><span class="sxs-lookup"><span data-stu-id="4f0e1-115">-Id</span></span>
<span data-ttu-id="4f0e1-116">소유자로 사용할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="4f0e1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f0e1-117">-PassThru</span></span>
<span data-ttu-id="4f0e1-118">결과로 업데이트된 소유자가 반환될 것 을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="4f0e1-119">-Path</span><span class="sxs-lookup"><span data-stu-id="4f0e1-119">-Path</span></span>
<span data-ttu-id="4f0e1-120">수정할 항목의 Data Lake Store 경로를 루트 디렉터리(/)로 시작하여 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4f0e1-121">-Type</span><span class="sxs-lookup"><span data-stu-id="4f0e1-121">-Type</span></span>
<span data-ttu-id="4f0e1-122">설정할 소유자의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="4f0e1-123">이 매개 변수에 허용되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="4f0e1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f0e1-124">-Confirm</span></span>
<span data-ttu-id="4f0e1-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f0e1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0e1-126">-WhatIf</span></span>
<span data-ttu-id="4f0e1-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4f0e1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0e1-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f0e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0e1-129">CommonParameters</span></span>
<span data-ttu-id="4f0e1-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0e1-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0e1-132">입력</span><span class="sxs-lookup"><span data-stu-id="4f0e1-132">INPUTS</span></span>

### <span data-ttu-id="4f0e1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4f0e1-133">System.String</span></span>

### <span data-ttu-id="4f0e1-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4f0e1-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4f0e1-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="4f0e1-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="4f0e1-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4f0e1-136">System.Guid</span></span>

### <span data-ttu-id="4f0e1-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f0e1-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f0e1-138">출력</span><span class="sxs-lookup"><span data-stu-id="4f0e1-138">OUTPUTS</span></span>

### <span data-ttu-id="4f0e1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4f0e1-139">System.String</span></span>

## <span data-ttu-id="4f0e1-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f0e1-140">NOTES</span></span>

## <span data-ttu-id="4f0e1-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f0e1-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f0e1-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="4f0e1-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)



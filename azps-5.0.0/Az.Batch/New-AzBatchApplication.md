---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217655"
---
# <span data-ttu-id="6e132-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6e132-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="6e132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e132-102">SYNOPSIS</span></span>
<span data-ttu-id="6e132-103">지정 된 Batch 계정에 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="6e132-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e132-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e132-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e132-105">DESCRIPTION</span></span>
<span data-ttu-id="6e132-106">**새 AzBatchApplication** cmdlet은 지정 된 Azure Batch 계정에 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="6e132-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e132-107">EXAMPLES</span></span>

### <span data-ttu-id="6e132-108">예제 1: 일괄 처리 계정에 빈 응용 프로그램 추가</span><span class="sxs-lookup"><span data-stu-id="6e132-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="6e132-109">이 명령은 ContosoBatch 계정에 Litware 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="6e132-110">응용 프로그램에는 처음에 패키지가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="6e132-111">변수</span><span class="sxs-lookup"><span data-stu-id="6e132-111">PARAMETERS</span></span>

### <span data-ttu-id="6e132-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e132-112">-AccountName</span></span>
<span data-ttu-id="6e132-113">이 cmdlet이 응용 프로그램을 추가 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e132-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="6e132-114">-AllowUpdates</span></span>
<span data-ttu-id="6e132-115">동일한 버전 문자열을 사용 하 여 응용 프로그램 내에서 패키지를 덮어쓸 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e132-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6e132-116">-ApplicationName</span></span>
<span data-ttu-id="6e132-117">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e132-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e132-118">-DefaultProfile</span></span>
<span data-ttu-id="6e132-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e132-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6e132-120">-DisplayName</span></span>
<span data-ttu-id="6e132-121">응용 프로그램의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e132-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e132-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e132-123">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-123">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e132-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e132-124">CommonParameters</span></span>
<span data-ttu-id="6e132-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e132-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e132-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e132-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e132-127">입력</span><span class="sxs-lookup"><span data-stu-id="6e132-127">INPUTS</span></span>

### <span data-ttu-id="6e132-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e132-128">System.String</span></span>

### <span data-ttu-id="6e132-129">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="6e132-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6e132-130">출력</span><span class="sxs-lookup"><span data-stu-id="6e132-130">OUTPUTS</span></span>

### <span data-ttu-id="6e132-131">Microsoft.Azure.Commands.Batch. PSApplication 모델</span><span class="sxs-lookup"><span data-stu-id="6e132-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="6e132-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6e132-132">NOTES</span></span>

## <span data-ttu-id="6e132-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e132-133">RELATED LINKS</span></span>

[<span data-ttu-id="6e132-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6e132-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="6e132-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6e132-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="6e132-136">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6e132-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="6e132-137">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6e132-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="6e132-138">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="6e132-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="6e132-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="6e132-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



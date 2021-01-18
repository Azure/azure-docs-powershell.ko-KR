---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494118"
---
# <span data-ttu-id="eda81-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eda81-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="eda81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda81-102">SYNOPSIS</span></span>
<span data-ttu-id="eda81-103">지정된 Batch 계정에 애플리케이션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="eda81-104">구문</span><span class="sxs-lookup"><span data-stu-id="eda81-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eda81-105">설명</span><span class="sxs-lookup"><span data-stu-id="eda81-105">DESCRIPTION</span></span>
<span data-ttu-id="eda81-106">**New-AzBatchApplication** cmdlet은 지정된 Azure Batch 계정에 애플리케이션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="eda81-107">예제</span><span class="sxs-lookup"><span data-stu-id="eda81-107">EXAMPLES</span></span>

### <span data-ttu-id="eda81-108">예제 1: Batch 계정에 빈 애플리케이션 추가</span><span class="sxs-lookup"><span data-stu-id="eda81-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="eda81-109">이 명령은 ContosoBatch 계정에 Litware 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="eda81-110">애플리케이션은 처음에 패키지를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="eda81-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eda81-111">PARAMETERS</span></span>

### <span data-ttu-id="eda81-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eda81-112">-AccountName</span></span>
<span data-ttu-id="eda81-113">이 cmdlet에서 애플리케이션을 추가하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="eda81-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="eda81-114">-AllowUpdates</span></span>
<span data-ttu-id="eda81-115">동일한 버전 문자열을 사용하여 애플리케이션 내의 패키지를 덮어 사용할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="eda81-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="eda81-116">-ApplicationName</span></span>
<span data-ttu-id="eda81-117">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="eda81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda81-118">-DefaultProfile</span></span>
<span data-ttu-id="eda81-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda81-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eda81-120">-DisplayName</span></span>
<span data-ttu-id="eda81-121">애플리케이션의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="eda81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda81-122">-ResourceGroupName</span></span>
<span data-ttu-id="eda81-123">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="eda81-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda81-124">CommonParameters</span></span>
<span data-ttu-id="eda81-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eda81-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda81-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eda81-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda81-127">입력</span><span class="sxs-lookup"><span data-stu-id="eda81-127">INPUTS</span></span>

### <span data-ttu-id="eda81-128">System.String</span><span class="sxs-lookup"><span data-stu-id="eda81-128">System.String</span></span>

### <span data-ttu-id="eda81-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="eda81-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="eda81-130">출력</span><span class="sxs-lookup"><span data-stu-id="eda81-130">OUTPUTS</span></span>

### <span data-ttu-id="eda81-131">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="eda81-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="eda81-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eda81-132">NOTES</span></span>

## <span data-ttu-id="eda81-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eda81-133">RELATED LINKS</span></span>

[<span data-ttu-id="eda81-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eda81-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="eda81-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eda81-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="eda81-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eda81-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="eda81-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eda81-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="eda81-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eda81-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="eda81-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eda81-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



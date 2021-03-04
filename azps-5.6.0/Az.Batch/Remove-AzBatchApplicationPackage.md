---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: 7c51776683d4a8ecb777fd56d8b83ca4ae672206
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969691"
---
# <span data-ttu-id="91648-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="91648-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="91648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91648-102">SYNOPSIS</span></span>
<span data-ttu-id="91648-103">애플리케이션 패키지 레코드 및 이진 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="91648-104">구문</span><span class="sxs-lookup"><span data-stu-id="91648-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91648-105">설명</span><span class="sxs-lookup"><span data-stu-id="91648-105">DESCRIPTION</span></span>
<span data-ttu-id="91648-106">**Remove-AzBatchApplicationPackage** cmdlet은 Azure Batch 계정에서 애플리케이션 패키지 레코드 및 이진 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="91648-107">예제</span><span class="sxs-lookup"><span data-stu-id="91648-107">EXAMPLES</span></span>

### <span data-ttu-id="91648-108">예제 1: Batch 계정에서 애플리케이션 패키지 삭제</span><span class="sxs-lookup"><span data-stu-id="91648-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="91648-109">이 명령은 ContosoBatchGroup 계정에서 Litware 애플리케이션의 버전 1.0을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="91648-110">명령은 패키지 레코드와 패키지 이진 파일을 포함하는 Blob을 모두 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="91648-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="91648-111">PARAMETERS</span></span>

### <span data-ttu-id="91648-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91648-112">-AccountName</span></span>
<span data-ttu-id="91648-113">이 cmdlet에서 애플리케이션 패키지를 삭제하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="91648-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="91648-114">-ApplicationName</span></span>
<span data-ttu-id="91648-115">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="91648-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="91648-116">-ApplicationVersion</span></span>
<span data-ttu-id="91648-117">애플리케이션의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91648-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91648-118">-DefaultProfile</span></span>
<span data-ttu-id="91648-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91648-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91648-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91648-120">-ResourceGroupName</span></span>
<span data-ttu-id="91648-121">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="91648-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91648-122">CommonParameters</span></span>
<span data-ttu-id="91648-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91648-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91648-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91648-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91648-125">입력</span><span class="sxs-lookup"><span data-stu-id="91648-125">INPUTS</span></span>

### <span data-ttu-id="91648-126">System.String</span><span class="sxs-lookup"><span data-stu-id="91648-126">System.String</span></span>

## <span data-ttu-id="91648-127">출력</span><span class="sxs-lookup"><span data-stu-id="91648-127">OUTPUTS</span></span>

### <span data-ttu-id="91648-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="91648-128">System.Void</span></span>

## <span data-ttu-id="91648-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91648-129">NOTES</span></span>

## <span data-ttu-id="91648-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91648-130">RELATED LINKS</span></span>

[<span data-ttu-id="91648-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="91648-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="91648-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="91648-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="91648-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="91648-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="91648-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="91648-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="91648-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="91648-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="91648-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="91648-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



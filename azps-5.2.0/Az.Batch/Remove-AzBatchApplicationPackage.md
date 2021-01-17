---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361257"
---
# <span data-ttu-id="ff538-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff538-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="ff538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff538-102">SYNOPSIS</span></span>
<span data-ttu-id="ff538-103">애플리케이션 패키지 레코드 및 이진 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="ff538-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff538-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff538-105">설명</span><span class="sxs-lookup"><span data-stu-id="ff538-105">DESCRIPTION</span></span>
<span data-ttu-id="ff538-106">**Remove-AzBatchApplicationPackage** cmdlet은 Azure Batch 계정에서 애플리케이션 패키지 레코드 및 이진 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="ff538-107">예제</span><span class="sxs-lookup"><span data-stu-id="ff538-107">EXAMPLES</span></span>

### <span data-ttu-id="ff538-108">예제 1: Batch 계정에서 애플리케이션 패키지 삭제</span><span class="sxs-lookup"><span data-stu-id="ff538-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="ff538-109">이 명령은 ContosoBatchGroup 계정에서 Litware 애플리케이션의 버전 1.0을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="ff538-110">이 명령은 패키지 레코드와 패키지 이진 파일을 포함하는 Blob을 모두 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="ff538-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff538-111">PARAMETERS</span></span>

### <span data-ttu-id="ff538-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff538-112">-AccountName</span></span>
<span data-ttu-id="ff538-113">이 cmdlet이 애플리케이션 패키지를 삭제하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="ff538-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ff538-114">-ApplicationName</span></span>
<span data-ttu-id="ff538-115">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="ff538-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="ff538-116">-ApplicationVersion</span></span>
<span data-ttu-id="ff538-117">애플리케이션의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="ff538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff538-118">-DefaultProfile</span></span>
<span data-ttu-id="ff538-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff538-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff538-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff538-121">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ff538-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff538-122">CommonParameters</span></span>
<span data-ttu-id="ff538-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff538-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff538-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff538-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff538-125">입력</span><span class="sxs-lookup"><span data-stu-id="ff538-125">INPUTS</span></span>

### <span data-ttu-id="ff538-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ff538-126">System.String</span></span>

## <span data-ttu-id="ff538-127">출력</span><span class="sxs-lookup"><span data-stu-id="ff538-127">OUTPUTS</span></span>

### <span data-ttu-id="ff538-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="ff538-128">System.Void</span></span>

## <span data-ttu-id="ff538-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff538-129">NOTES</span></span>

## <span data-ttu-id="ff538-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff538-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff538-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff538-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="ff538-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff538-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="ff538-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff538-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="ff538-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff538-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ff538-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff538-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ff538-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff538-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



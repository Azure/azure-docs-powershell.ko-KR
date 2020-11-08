---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217073"
---
# <span data-ttu-id="ff724-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff724-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="ff724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff724-102">SYNOPSIS</span></span>
<span data-ttu-id="ff724-103">응용 프로그램 패키지 레코드와 이진 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="ff724-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff724-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff724-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff724-105">DESCRIPTION</span></span>
<span data-ttu-id="ff724-106">**AzBatchApplicationPackage** cmdlet은 앱 패키지 레코드와 Azure Batch 계정에서 바이너리 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="ff724-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff724-107">EXAMPLES</span></span>

### <span data-ttu-id="ff724-108">예제 1: 일괄 처리 계정에서 응용 프로그램 패키지 삭제</span><span class="sxs-lookup"><span data-stu-id="ff724-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="ff724-109">이 명령은 ContosoBatchGroup 계정에서 Litware 응용 프로그램의 버전 1.0을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="ff724-110">이 명령은 패키지 레코드와 패키지 이진 파일을 포함 하는 blob을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="ff724-111">변수</span><span class="sxs-lookup"><span data-stu-id="ff724-111">PARAMETERS</span></span>

### <span data-ttu-id="ff724-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff724-112">-AccountName</span></span>
<span data-ttu-id="ff724-113">이 cmdlet이 응용 프로그램 패키지를 삭제 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="ff724-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ff724-114">-ApplicationName</span></span>
<span data-ttu-id="ff724-115">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="ff724-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="ff724-116">-ApplicationVersion</span></span>
<span data-ttu-id="ff724-117">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="ff724-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff724-118">-DefaultProfile</span></span>
<span data-ttu-id="ff724-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff724-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff724-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff724-121">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ff724-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff724-122">CommonParameters</span></span>
<span data-ttu-id="ff724-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff724-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff724-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff724-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff724-125">입력</span><span class="sxs-lookup"><span data-stu-id="ff724-125">INPUTS</span></span>

### <span data-ttu-id="ff724-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff724-126">System.String</span></span>

## <span data-ttu-id="ff724-127">출력</span><span class="sxs-lookup"><span data-stu-id="ff724-127">OUTPUTS</span></span>

### <span data-ttu-id="ff724-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ff724-128">System.Void</span></span>

## <span data-ttu-id="ff724-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ff724-129">NOTES</span></span>

## <span data-ttu-id="ff724-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff724-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff724-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff724-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="ff724-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff724-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="ff724-133">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff724-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="ff724-134">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ff724-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ff724-135">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff724-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ff724-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ff724-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



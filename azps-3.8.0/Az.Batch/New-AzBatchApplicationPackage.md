---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042445"
---
# <span data-ttu-id="13906-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="13906-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="13906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13906-102">SYNOPSIS</span></span>
<span data-ttu-id="13906-103">일괄 처리 계정에 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13906-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="13906-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13906-104">SYNTAX</span></span>

### <span data-ttu-id="13906-105">UploadAndActivate (기본값)</span><span class="sxs-lookup"><span data-stu-id="13906-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13906-106">고만</span><span class="sxs-lookup"><span data-stu-id="13906-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13906-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13906-107">DESCRIPTION</span></span>
<span data-ttu-id="13906-108">**새 AzBatchApplicationPackage** Cmdlet은 Azure Batch 계정에서 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13906-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="13906-109">예제의</span><span class="sxs-lookup"><span data-stu-id="13906-109">EXAMPLES</span></span>

### <span data-ttu-id="13906-110">예제 1: 일괄 처리 계정에 응용 프로그램 패키지 설치</span><span class="sxs-lookup"><span data-stu-id="13906-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="13906-111">이 명령은 Litware 응용 프로그램의 버전 1.0를 만들고 활성화 하 고 litware.1.0.zip의 콘텐츠를 응용 프로그램 패키지 콘텐츠로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="13906-112">변수</span><span class="sxs-lookup"><span data-stu-id="13906-112">PARAMETERS</span></span>

### <span data-ttu-id="13906-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13906-113">-AccountName</span></span>
<span data-ttu-id="13906-114">이 cmdlet이 응용 프로그램 패키지를 추가 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="13906-115">-고 대만</span><span class="sxs-lookup"><span data-stu-id="13906-115">-ActivateOnly</span></span>
<span data-ttu-id="13906-116">이 cmdlet이 이미 업로드 된 응용 프로그램 패키지를 활성화 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13906-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13906-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="13906-117">-ApplicationName</span></span>
<span data-ttu-id="13906-118">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="13906-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="13906-119">-ApplicationVersion</span></span>
<span data-ttu-id="13906-120">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="13906-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13906-121">-DefaultProfile</span></span>
<span data-ttu-id="13906-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13906-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13906-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="13906-123">-FilePath</span></span>
<span data-ttu-id="13906-124">업로드할 파일을 응용 프로그램 패키지 이진 파일로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13906-125">-형식</span><span class="sxs-lookup"><span data-stu-id="13906-125">-Format</span></span>
<span data-ttu-id="13906-126">응용 프로그램 패키지 이진 파일의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13906-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13906-127">-ResourceGroupName</span></span>
<span data-ttu-id="13906-128">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="13906-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13906-129">CommonParameters</span></span>
<span data-ttu-id="13906-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13906-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13906-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13906-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13906-132">입력</span><span class="sxs-lookup"><span data-stu-id="13906-132">INPUTS</span></span>

### <span data-ttu-id="13906-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13906-133">System.String</span></span>

### <span data-ttu-id="13906-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13906-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13906-135">출력</span><span class="sxs-lookup"><span data-stu-id="13906-135">OUTPUTS</span></span>

### <span data-ttu-id="13906-136">Microsoft.Azure.Commands.Batch. PSApplicationPackage 모델</span><span class="sxs-lookup"><span data-stu-id="13906-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="13906-137">상속자</span><span class="sxs-lookup"><span data-stu-id="13906-137">NOTES</span></span>

## <span data-ttu-id="13906-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13906-138">RELATED LINKS</span></span>

[<span data-ttu-id="13906-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="13906-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="13906-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="13906-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="13906-141">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="13906-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="13906-142">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="13906-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="13906-143">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="13906-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="13906-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="13906-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



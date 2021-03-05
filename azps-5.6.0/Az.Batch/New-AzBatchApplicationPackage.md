---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 766f521f5e963f05e51cd000361675a2f81bbb1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960891"
---
# <span data-ttu-id="a42f7-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a42f7-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="a42f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a42f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a42f7-103">Batch 계정에 애플리케이션 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="a42f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="a42f7-104">SYNTAX</span></span>

### <span data-ttu-id="a42f7-105">UploadAndActivate(기본값)</span><span class="sxs-lookup"><span data-stu-id="a42f7-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a42f7-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="a42f7-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a42f7-107">설명</span><span class="sxs-lookup"><span data-stu-id="a42f7-107">DESCRIPTION</span></span>
<span data-ttu-id="a42f7-108">**New-AzBatchApplicationPackage** cmdlet은 Azure Batch 계정에 애플리케이션 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="a42f7-109">예제</span><span class="sxs-lookup"><span data-stu-id="a42f7-109">EXAMPLES</span></span>

### <span data-ttu-id="a42f7-110">예제 1: Batch 계정에 애플리케이션 패키지 설치</span><span class="sxs-lookup"><span data-stu-id="a42f7-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="a42f7-111">이 명령은 Litware 애플리케이션의 버전 1.0을 만들고 활성화하고 애플리케이션 litware.1.0.zip 콘텐츠로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="a42f7-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a42f7-112">PARAMETERS</span></span>

### <span data-ttu-id="a42f7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a42f7-113">-AccountName</span></span>
<span data-ttu-id="a42f7-114">이 cmdlet에서 애플리케이션 패키지를 추가하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="a42f7-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="a42f7-115">-ActivateOnly</span></span>
<span data-ttu-id="a42f7-116">이 cmdlet은 이미 업로드된 애플리케이션 패키지를 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="a42f7-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a42f7-117">-ApplicationName</span></span>
<span data-ttu-id="a42f7-118">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="a42f7-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="a42f7-119">-ApplicationVersion</span></span>
<span data-ttu-id="a42f7-120">애플리케이션의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="a42f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42f7-121">-DefaultProfile</span></span>
<span data-ttu-id="a42f7-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a42f7-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a42f7-123">-FilePath</span></span>
<span data-ttu-id="a42f7-124">애플리케이션 패키지 이진 파일로 업로드할 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="a42f7-125">-Format</span><span class="sxs-lookup"><span data-stu-id="a42f7-125">-Format</span></span>
<span data-ttu-id="a42f7-126">애플리케이션 패키지 이진 파일의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="a42f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="a42f7-128">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a42f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42f7-129">CommonParameters</span></span>
<span data-ttu-id="a42f7-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a42f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42f7-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a42f7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42f7-132">입력</span><span class="sxs-lookup"><span data-stu-id="a42f7-132">INPUTS</span></span>

### <span data-ttu-id="a42f7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a42f7-133">System.String</span></span>

### <span data-ttu-id="a42f7-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a42f7-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a42f7-135">출력</span><span class="sxs-lookup"><span data-stu-id="a42f7-135">OUTPUTS</span></span>

### <span data-ttu-id="a42f7-136">Microsoft.Azure.Commands.Bat. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a42f7-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="a42f7-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a42f7-137">NOTES</span></span>

## <span data-ttu-id="a42f7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a42f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="a42f7-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a42f7-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a42f7-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a42f7-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="a42f7-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a42f7-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="a42f7-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a42f7-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a42f7-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a42f7-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="a42f7-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a42f7-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



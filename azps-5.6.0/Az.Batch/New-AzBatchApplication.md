---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: e22c1ef6a95fafe21f0fd10a47a67098976395e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966747"
---
# <span data-ttu-id="aa0de-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="aa0de-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="aa0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa0de-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0de-103">지정된 Batch 계정에 애플리케이션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="aa0de-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa0de-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa0de-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa0de-105">DESCRIPTION</span></span>
<span data-ttu-id="aa0de-106">**New-AzBatchApplication** cmdlet은 지정된 Azure Batch 계정에 애플리케이션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="aa0de-107">예제</span><span class="sxs-lookup"><span data-stu-id="aa0de-107">EXAMPLES</span></span>

### <span data-ttu-id="aa0de-108">예제 1: Batch 계정에 빈 애플리케이션 추가</span><span class="sxs-lookup"><span data-stu-id="aa0de-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="aa0de-109">이 명령은 ContosoBatch 계정에 Litware 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="aa0de-110">애플리케이션에 처음에는 패키지가 포함되어 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="aa0de-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa0de-111">PARAMETERS</span></span>

### <span data-ttu-id="aa0de-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa0de-112">-AccountName</span></span>
<span data-ttu-id="aa0de-113">이 cmdlet에서 애플리케이션을 추가하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="aa0de-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="aa0de-114">-AllowUpdates</span></span>
<span data-ttu-id="aa0de-115">애플리케이션 내의 패키지가 동일한 버전 문자열을 사용하여 덮어질 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="aa0de-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="aa0de-116">-ApplicationName</span></span>
<span data-ttu-id="aa0de-117">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="aa0de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0de-118">-DefaultProfile</span></span>
<span data-ttu-id="aa0de-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa0de-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa0de-120">-DisplayName</span></span>
<span data-ttu-id="aa0de-121">애플리케이션의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="aa0de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0de-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa0de-123">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="aa0de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0de-124">CommonParameters</span></span>
<span data-ttu-id="aa0de-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0de-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa0de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0de-127">입력</span><span class="sxs-lookup"><span data-stu-id="aa0de-127">INPUTS</span></span>

### <span data-ttu-id="aa0de-128">System.String</span><span class="sxs-lookup"><span data-stu-id="aa0de-128">System.String</span></span>

### <span data-ttu-id="aa0de-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="aa0de-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="aa0de-130">출력</span><span class="sxs-lookup"><span data-stu-id="aa0de-130">OUTPUTS</span></span>

### <span data-ttu-id="aa0de-131">Microsoft.Azure.Commands.Bat. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="aa0de-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="aa0de-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa0de-132">NOTES</span></span>

## <span data-ttu-id="aa0de-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa0de-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa0de-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="aa0de-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="aa0de-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="aa0de-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="aa0de-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="aa0de-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="aa0de-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="aa0de-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="aa0de-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="aa0de-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="aa0de-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="aa0de-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: b32c0d7db6a55a560733380c66e971c614fabc71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972208"
---
# <span data-ttu-id="7f6dd-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7f6dd-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="7f6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6dd-103">지정된 애플리케이션에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="7f6dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f6dd-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6dd-105">설명</span><span class="sxs-lookup"><span data-stu-id="7f6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6dd-106">**Get-AzBatchApplication** cmdlet은 Azure Batch 계정의 애플리케이션에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="7f6dd-107">예제</span><span class="sxs-lookup"><span data-stu-id="7f6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6dd-108">예제 1: Batch 계정에 애플리케이션 표시</span><span class="sxs-lookup"><span data-stu-id="7f6dd-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="7f6dd-109">이 명령은 ContosoBatch 계정에 모든 애플리케이션을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="7f6dd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f6dd-110">PARAMETERS</span></span>

### <span data-ttu-id="7f6dd-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f6dd-111">-AccountName</span></span>
<span data-ttu-id="7f6dd-112">애플리케이션을 포함하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="7f6dd-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="7f6dd-113">-ApplicationName</span></span>
<span data-ttu-id="7f6dd-114">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6dd-115">-DefaultProfile</span></span>
<span data-ttu-id="7f6dd-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f6dd-118">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="7f6dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6dd-119">CommonParameters</span></span>
<span data-ttu-id="7f6dd-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6dd-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f6dd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6dd-122">입력</span><span class="sxs-lookup"><span data-stu-id="7f6dd-122">INPUTS</span></span>

### <span data-ttu-id="7f6dd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7f6dd-123">System.String</span></span>

## <span data-ttu-id="7f6dd-124">출력</span><span class="sxs-lookup"><span data-stu-id="7f6dd-124">OUTPUTS</span></span>

### <span data-ttu-id="7f6dd-125">Microsoft.Azure.Commands.Bat. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="7f6dd-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="7f6dd-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f6dd-126">NOTES</span></span>

## <span data-ttu-id="7f6dd-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f6dd-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f6dd-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7f6dd-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="7f6dd-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7f6dd-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="7f6dd-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7f6dd-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="7f6dd-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7f6dd-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="7f6dd-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7f6dd-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="7f6dd-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7f6dd-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



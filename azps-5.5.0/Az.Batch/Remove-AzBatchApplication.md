---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195241"
---
# <span data-ttu-id="77e62-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77e62-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="77e62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e62-102">SYNOPSIS</span></span>
<span data-ttu-id="77e62-103">Batch 계정에서 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="77e62-104">구문</span><span class="sxs-lookup"><span data-stu-id="77e62-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e62-105">설명</span><span class="sxs-lookup"><span data-stu-id="77e62-105">DESCRIPTION</span></span>
<span data-ttu-id="77e62-106">**Remove-AzBatchApplication** cmdlet은 Azure Batch 계정에서 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="77e62-107">예제</span><span class="sxs-lookup"><span data-stu-id="77e62-107">EXAMPLES</span></span>

### <span data-ttu-id="77e62-108">예제 1: Batch 계정에서 애플리케이션 삭제</span><span class="sxs-lookup"><span data-stu-id="77e62-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="77e62-109">이 명령은 ContosoBatch 계정에서 Litware 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="77e62-110">애플리케이션에 패키지가 포함되어 있는 경우 명령이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="77e62-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77e62-111">PARAMETERS</span></span>

### <span data-ttu-id="77e62-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77e62-112">-AccountName</span></span>
<span data-ttu-id="77e62-113">이 cmdlet이 애플리케이션을 제거하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="77e62-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="77e62-114">-ApplicationName</span></span>
<span data-ttu-id="77e62-115">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="77e62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e62-116">-DefaultProfile</span></span>
<span data-ttu-id="77e62-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e62-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e62-118">-ResourceGroupName</span></span>
<span data-ttu-id="77e62-119">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="77e62-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e62-120">CommonParameters</span></span>
<span data-ttu-id="77e62-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77e62-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e62-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77e62-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e62-123">입력</span><span class="sxs-lookup"><span data-stu-id="77e62-123">INPUTS</span></span>

### <span data-ttu-id="77e62-124">System.String</span><span class="sxs-lookup"><span data-stu-id="77e62-124">System.String</span></span>

## <span data-ttu-id="77e62-125">출력</span><span class="sxs-lookup"><span data-stu-id="77e62-125">OUTPUTS</span></span>

### <span data-ttu-id="77e62-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="77e62-126">System.Void</span></span>

## <span data-ttu-id="77e62-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77e62-127">NOTES</span></span>

## <span data-ttu-id="77e62-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77e62-128">RELATED LINKS</span></span>

[<span data-ttu-id="77e62-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77e62-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="77e62-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77e62-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="77e62-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77e62-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="77e62-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77e62-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="77e62-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="77e62-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="77e62-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="77e62-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



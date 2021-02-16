---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187865"
---
# <span data-ttu-id="48f66-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48f66-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="48f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f66-102">SYNOPSIS</span></span>
<span data-ttu-id="48f66-103">디바이스에 새 Edge Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="48f66-104">구문</span><span class="sxs-lookup"><span data-stu-id="48f66-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f66-105">설명</span><span class="sxs-lookup"><span data-stu-id="48f66-105">DESCRIPTION</span></span>
<span data-ttu-id="48f66-106">**New-AzStackEdgeStorageAccount** cmdlet은 Stack Edge 디바이스에 새 Edge Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="48f66-107">디바이스의 경우 하나의 Edge Storage 계정을 하나의 Cloud Storage 계정에만 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="48f66-108">예제</span><span class="sxs-lookup"><span data-stu-id="48f66-108">EXAMPLES</span></span>

### <span data-ttu-id="48f66-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="48f66-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="48f66-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="48f66-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="48f66-111">디바이스의 2 EdgeStorageAccounts는 1개 이상의 Cloud Storage 계정을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="48f66-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48f66-112">PARAMETERS</span></span>

### <span data-ttu-id="48f66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48f66-113">-AsJob</span></span>
<span data-ttu-id="48f66-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="48f66-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="48f66-115">-Cloud</span></span>
<span data-ttu-id="48f66-116">계층화에 CloudStorageAccount를 사용</span><span class="sxs-lookup"><span data-stu-id="48f66-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f66-117">-DefaultProfile</span></span>
<span data-ttu-id="48f66-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48f66-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="48f66-119">-DeviceName</span></span>
<span data-ttu-id="48f66-120">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="48f66-120">Device Name</span></span>

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

### <span data-ttu-id="48f66-121">-Name</span><span class="sxs-lookup"><span data-stu-id="48f66-121">-Name</span></span>
<span data-ttu-id="48f66-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="48f66-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f66-123">-ResourceGroupName</span></span>
<span data-ttu-id="48f66-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="48f66-124">Resource Group Name</span></span>

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

### <span data-ttu-id="48f66-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="48f66-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="48f66-126">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="48f66-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48f66-127">-Confirm</span></span>
<span data-ttu-id="48f66-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f66-129">-WhatIf</span></span>
<span data-ttu-id="48f66-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="48f66-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48f66-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f66-132">CommonParameters</span></span>
<span data-ttu-id="48f66-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48f66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f66-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48f66-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f66-135">입력</span><span class="sxs-lookup"><span data-stu-id="48f66-135">INPUTS</span></span>

### <span data-ttu-id="48f66-136">System.String</span><span class="sxs-lookup"><span data-stu-id="48f66-136">System.String</span></span>

### <span data-ttu-id="48f66-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48f66-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48f66-138">출력</span><span class="sxs-lookup"><span data-stu-id="48f66-138">OUTPUTS</span></span>

### <span data-ttu-id="48f66-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48f66-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="48f66-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48f66-140">NOTES</span></span>

## <span data-ttu-id="48f66-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48f66-141">RELATED LINKS</span></span>

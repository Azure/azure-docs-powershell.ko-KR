---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212549"
---
# <span data-ttu-id="2c547-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c547-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="2c547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c547-102">SYNOPSIS</span></span>
<span data-ttu-id="2c547-103">장치에 새 Edge 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="2c547-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c547-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c547-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c547-105">DESCRIPTION</span></span>
<span data-ttu-id="2c547-106">**AzDataBoxEdgeStorageAccount** Cmdlet은 데이터 상자 가장자리 장치에 새 Edge 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="2c547-107">장치의 경우 한 Edge 저장소 계정을 최대 하나의 클라우드 저장소 계정에만 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="2c547-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2c547-108">EXAMPLES</span></span>

### <span data-ttu-id="2c547-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c547-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="2c547-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c547-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="2c547-111">2 EdgeStorageAccounts 장치에서 1 개 이상의 클라우드 저장소 계정을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="2c547-112">변수</span><span class="sxs-lookup"><span data-stu-id="2c547-112">PARAMETERS</span></span>

### <span data-ttu-id="2c547-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c547-113">-AsJob</span></span>
<span data-ttu-id="2c547-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2c547-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c547-115">-클라우드</span><span class="sxs-lookup"><span data-stu-id="2c547-115">-Cloud</span></span>
<span data-ttu-id="2c547-116">은 (는) tiering Storageaccount를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="2c547-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c547-117">-DefaultProfile</span></span>
<span data-ttu-id="2c547-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c547-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="2c547-119">-DeviceName</span></span>
<span data-ttu-id="2c547-120">장치 이름</span><span class="sxs-lookup"><span data-stu-id="2c547-120">Device Name</span></span>

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

### <span data-ttu-id="2c547-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2c547-121">-Name</span></span>
<span data-ttu-id="2c547-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="2c547-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c547-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c547-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c547-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2c547-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2c547-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="2c547-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="2c547-126">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="2c547-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="2c547-127">-확인</span><span class="sxs-lookup"><span data-stu-id="2c547-127">-Confirm</span></span>
<span data-ttu-id="2c547-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c547-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c547-129">-WhatIf</span></span>
<span data-ttu-id="2c547-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c547-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c547-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c547-132">CommonParameters</span></span>
<span data-ttu-id="2c547-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c547-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c547-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c547-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c547-135">입력</span><span class="sxs-lookup"><span data-stu-id="2c547-135">INPUTS</span></span>

### <span data-ttu-id="2c547-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c547-136">System.String</span></span>

### <span data-ttu-id="2c547-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c547-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c547-138">출력</span><span class="sxs-lookup"><span data-stu-id="2c547-138">OUTPUTS</span></span>

### <span data-ttu-id="2c547-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c547-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="2c547-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2c547-140">NOTES</span></span>

## <span data-ttu-id="2c547-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c547-141">RELATED LINKS</span></span>

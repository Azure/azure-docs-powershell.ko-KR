---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044698"
---
# <span data-ttu-id="db4f9-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="db4f9-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="db4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="db4f9-103">복제 될 vMWare 가상 머신 디스크에 대 한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="db4f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db4f9-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db4f9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="db4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="db4f9-106">디스크를 복제 하는 데 사용 되는 캐시 저장소 계정 및 대상 관리 디스크 형식 (복구 영역)에 vMWare 가상 머신 디스크를 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="db4f9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="db4f9-107">EXAMPLES</span></span>

### <span data-ttu-id="db4f9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="db4f9-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="db4f9-109">복제할 vMWare 가상 머신 디스크에 대 한 디스크 매핑 개체를 만듭니다. VMWare 컴퓨터용 보호 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="db4f9-110">변수</span><span class="sxs-lookup"><span data-stu-id="db4f9-110">PARAMETERS</span></span>

### <span data-ttu-id="db4f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4f9-111">-DefaultProfile</span></span>
<span data-ttu-id="db4f9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db4f9-113">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="db4f9-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="db4f9-114">관리 되는 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4f9-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="db4f9-115">-DiskId</span></span>
<span data-ttu-id="db4f9-116">이 매핑이 해당 하는 디스크의 DiskId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4f9-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="db4f9-117">-DiskType</span></span>
<span data-ttu-id="db4f9-118">복구 디스크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-118">Specifies the Recovery disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4f9-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="db4f9-119">-LogStorageAccountId</span></span>
<span data-ttu-id="db4f9-120">복제 로그를 저장 하는 데 사용할 로그 또는 캐시 저장소 계정 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4f9-121">-확인</span><span class="sxs-lookup"><span data-stu-id="db4f9-121">-Confirm</span></span>
<span data-ttu-id="db4f9-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db4f9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db4f9-123">-WhatIf</span></span>
<span data-ttu-id="db4f9-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db4f9-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db4f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4f9-126">CommonParameters</span></span>
<span data-ttu-id="db4f9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db4f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4f9-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db4f9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4f9-129">입력</span><span class="sxs-lookup"><span data-stu-id="db4f9-129">INPUTS</span></span>

### <span data-ttu-id="db4f9-130">않아야</span><span class="sxs-lookup"><span data-stu-id="db4f9-130">None</span></span>

## <span data-ttu-id="db4f9-131">출력</span><span class="sxs-lookup"><span data-stu-id="db4f9-131">OUTPUTS</span></span>

### <span data-ttu-id="db4f9-132">SiteRecovery. AsrInMageAzureV2DiskInput에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="db4f9-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="db4f9-133">상속자</span><span class="sxs-lookup"><span data-stu-id="db4f9-133">NOTES</span></span>

## <span data-ttu-id="db4f9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db4f9-134">RELATED LINKS</span></span>

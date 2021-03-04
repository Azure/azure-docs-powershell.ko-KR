---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 857bc438d1c51b28e3ead1095ca4722fce7ccc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958043"
---
# <span data-ttu-id="80954-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="80954-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="80954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80954-102">SYNOPSIS</span></span>
<span data-ttu-id="80954-103">복제할 vMWare 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80954-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="80954-104">구문</span><span class="sxs-lookup"><span data-stu-id="80954-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80954-105">설명</span><span class="sxs-lookup"><span data-stu-id="80954-105">DESCRIPTION</span></span>
<span data-ttu-id="80954-106">vMWare 가상 머신 디스크를 캐시 저장소 계정에 매핑하고 디스크를 복제하는 데 사용할 관리 디스크 유형(복구 지역)을 대상으로 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80954-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="80954-107">예제</span><span class="sxs-lookup"><span data-stu-id="80954-107">EXAMPLES</span></span>

### <span data-ttu-id="80954-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="80954-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="80954-109">복제할 vMWare 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다. vMWare 머신에 대한 보호를 사용하도록 설정하는 동안 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="80954-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="80954-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="80954-110">PARAMETERS</span></span>

### <span data-ttu-id="80954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80954-111">-DefaultProfile</span></span>
<span data-ttu-id="80954-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80954-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80954-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="80954-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="80954-114">관리 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80954-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="80954-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="80954-115">-DiskId</span></span>
<span data-ttu-id="80954-116">이 매핑에 해당하는 디스크의 DiskId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80954-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="80954-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="80954-117">-DiskType</span></span>
<span data-ttu-id="80954-118">복구 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80954-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="80954-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="80954-119">-LogStorageAccountId</span></span>
<span data-ttu-id="80954-120">복제 로그를 저장하는 데 사용할 로그 또는 캐시 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80954-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="80954-121">-확인</span><span class="sxs-lookup"><span data-stu-id="80954-121">-Confirm</span></span>
<span data-ttu-id="80954-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80954-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80954-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80954-123">-WhatIf</span></span>
<span data-ttu-id="80954-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="80954-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80954-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80954-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80954-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80954-126">CommonParameters</span></span>
<span data-ttu-id="80954-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80954-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80954-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80954-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80954-129">입력</span><span class="sxs-lookup"><span data-stu-id="80954-129">INPUTS</span></span>

### <span data-ttu-id="80954-130">없음</span><span class="sxs-lookup"><span data-stu-id="80954-130">None</span></span>

## <span data-ttu-id="80954-131">출력</span><span class="sxs-lookup"><span data-stu-id="80954-131">OUTPUTS</span></span>

### <span data-ttu-id="80954-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="80954-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="80954-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80954-133">NOTES</span></span>

## <span data-ttu-id="80954-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80954-134">RELATED LINKS</span></span>

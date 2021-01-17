---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362643"
---
# <span data-ttu-id="6d70b-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="6d70b-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="6d70b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d70b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d70b-103">복제할 vMWare 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="6d70b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d70b-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d70b-105">설명</span><span class="sxs-lookup"><span data-stu-id="6d70b-105">DESCRIPTION</span></span>
<span data-ttu-id="6d70b-106">vMWare 가상 머신 디스크를 캐시 저장소 계정에 매핑하고 디스크를 복제하는 데 사용할 대상 관리 디스크 유형(복구 지역)에 매핑하는 디스크 매핑 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="6d70b-107">예제</span><span class="sxs-lookup"><span data-stu-id="6d70b-107">EXAMPLES</span></span>

### <span data-ttu-id="6d70b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d70b-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="6d70b-109">복제할 vMWare 가상 머신 디스크에 대한 디스크 매핑 개체를 만듭니다. vMWare 머신에 대한 보호를 사용하도록 설정하는 동안 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="6d70b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d70b-110">PARAMETERS</span></span>

### <span data-ttu-id="6d70b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d70b-111">-DefaultProfile</span></span>
<span data-ttu-id="6d70b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d70b-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6d70b-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6d70b-114">관리 디스크의 암호화에 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="6d70b-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="6d70b-115">-DiskId</span></span>
<span data-ttu-id="6d70b-116">이 매핑에 해당하는 디스크의 DiskId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="6d70b-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="6d70b-117">-DiskType</span></span>
<span data-ttu-id="6d70b-118">복구 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="6d70b-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6d70b-119">-LogStorageAccountId</span></span>
<span data-ttu-id="6d70b-120">복제 로그를 저장하는 데 사용할 로그 또는 캐시 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="6d70b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d70b-121">-Confirm</span></span>
<span data-ttu-id="6d70b-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d70b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d70b-123">-WhatIf</span></span>
<span data-ttu-id="6d70b-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6d70b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d70b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d70b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d70b-126">CommonParameters</span></span>
<span data-ttu-id="6d70b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d70b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d70b-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d70b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d70b-129">입력</span><span class="sxs-lookup"><span data-stu-id="6d70b-129">INPUTS</span></span>

### <span data-ttu-id="6d70b-130">없음</span><span class="sxs-lookup"><span data-stu-id="6d70b-130">None</span></span>

## <span data-ttu-id="6d70b-131">출력</span><span class="sxs-lookup"><span data-stu-id="6d70b-131">OUTPUTS</span></span>

### <span data-ttu-id="6d70b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="6d70b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="6d70b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d70b-133">NOTES</span></span>

## <span data-ttu-id="6d70b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d70b-134">RELATED LINKS</span></span>

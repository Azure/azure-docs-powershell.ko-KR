---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206184"
---
# <span data-ttu-id="71881-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71881-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="71881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71881-102">SYNOPSIS</span></span>
<span data-ttu-id="71881-103">지정된 ASR 저장소 분류 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="71881-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="71881-104">구문</span><span class="sxs-lookup"><span data-stu-id="71881-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71881-105">설명</span><span class="sxs-lookup"><span data-stu-id="71881-105">DESCRIPTION</span></span>
<span data-ttu-id="71881-106">**Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet은 지정된 Azure Site Recovery 저장소 분류 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="71881-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="71881-107">예제</span><span class="sxs-lookup"><span data-stu-id="71881-107">EXAMPLES</span></span>

### <span data-ttu-id="71881-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="71881-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="71881-109">지정된 저장소 분류 매핑의 지우기 시작 및 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71881-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="71881-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71881-110">PARAMETERS</span></span>

### <span data-ttu-id="71881-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71881-111">-DefaultProfile</span></span>
<span data-ttu-id="71881-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71881-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71881-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71881-113">-InputObject</span></span>
<span data-ttu-id="71881-114">cmdlet에 대한 입력 개체: 삭제할 ASR 저장소 분류 매핑에 해당하는 ASR 저장소 분류 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71881-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71881-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71881-115">-Confirm</span></span>
<span data-ttu-id="71881-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71881-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71881-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71881-117">-WhatIf</span></span>
<span data-ttu-id="71881-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71881-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71881-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71881-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71881-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71881-120">CommonParameters</span></span>
<span data-ttu-id="71881-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71881-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71881-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71881-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71881-123">입력</span><span class="sxs-lookup"><span data-stu-id="71881-123">INPUTS</span></span>

### <span data-ttu-id="71881-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71881-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="71881-125">출력</span><span class="sxs-lookup"><span data-stu-id="71881-125">OUTPUTS</span></span>

### <span data-ttu-id="71881-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="71881-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71881-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71881-127">NOTES</span></span>

## <span data-ttu-id="71881-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71881-128">RELATED LINKS</span></span>

[<span data-ttu-id="71881-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71881-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="71881-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71881-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

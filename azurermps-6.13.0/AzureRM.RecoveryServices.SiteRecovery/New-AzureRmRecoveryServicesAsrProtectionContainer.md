---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: b551e89a800c70f1321a1f58cf4d5eae39fe69e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524316"
---
# <span data-ttu-id="b5f58-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b5f58-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="b5f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f58-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f58-103">지정 된 패브릭 내에 Azure Site Recovery 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5f58-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5f58-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f58-106">New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet은 지정 된 Azure Site Recovery 패브릭 아래에 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="b5f58-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5f58-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f58-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5f58-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="b5f58-109">지정 된 매개 변수를 사용 하 여 보호 컨테이너 만들기를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b5f58-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5f58-110">PARAMETERS</span></span>

### <span data-ttu-id="b5f58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f58-111">-DefaultProfile</span></span>
<span data-ttu-id="b5f58-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f58-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f58-113">-InputObject</span></span>
<span data-ttu-id="b5f58-114">지정 된 입력 개체 (Azure Fabric)에서 복제 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f58-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b5f58-115">-Name</span></span>
<span data-ttu-id="b5f58-116">보호 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="b5f58-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b5f58-117">-Confirm</span></span>
<span data-ttu-id="b5f58-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f58-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f58-119">-WhatIf</span></span>
<span data-ttu-id="b5f58-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f58-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f58-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f58-122">CommonParameters</span></span>
<span data-ttu-id="b5f58-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5f58-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f58-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f58-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f58-125">입력</span><span class="sxs-lookup"><span data-stu-id="b5f58-125">INPUTS</span></span>

### <span data-ttu-id="b5f58-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="b5f58-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b5f58-127">출력</span><span class="sxs-lookup"><span data-stu-id="b5f58-127">OUTPUTS</span></span>

### <span data-ttu-id="b5f58-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="b5f58-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5f58-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b5f58-129">NOTES</span></span>

## <span data-ttu-id="b5f58-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5f58-130">RELATED LINKS</span></span>

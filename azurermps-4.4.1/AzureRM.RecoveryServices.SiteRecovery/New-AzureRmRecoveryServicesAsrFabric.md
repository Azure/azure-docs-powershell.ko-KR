---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711244"
---
# <span data-ttu-id="7e791-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e791-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="7e791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e791-102">SYNOPSIS</span></span>
<span data-ttu-id="7e791-103">Azure Site Recovery 패브릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e791-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e791-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e791-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e791-105">DESCRIPTION</span></span>
<span data-ttu-id="7e791-106">**AzureRmRecoveryServicesAsrFabric** cmdlet은 지정 된 형식의 Azure Site Recovery Fabric을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="7e791-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e791-107">EXAMPLES</span></span>

### <span data-ttu-id="7e791-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e791-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="7e791-109">전달 된 이름으로 패브릭 만들기를 시작 하 고 패브릭 만들기 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="7e791-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e791-110">PARAMETERS</span></span>

### <span data-ttu-id="7e791-111">-이름</span><span class="sxs-lookup"><span data-stu-id="7e791-111">-Name</span></span>
<span data-ttu-id="7e791-112">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e791-113">-Type</span><span class="sxs-lookup"><span data-stu-id="7e791-113">-Type</span></span>
<span data-ttu-id="7e791-114">Azure Site Recovery 패브릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e791-115">-확인</span><span class="sxs-lookup"><span data-stu-id="7e791-115">-Confirm</span></span>
<span data-ttu-id="7e791-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e791-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e791-117">-WhatIf</span></span>
<span data-ttu-id="7e791-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e791-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e791-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e791-120">CommonParameters</span></span>
<span data-ttu-id="7e791-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e791-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e791-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e791-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e791-123">입력</span><span class="sxs-lookup"><span data-stu-id="7e791-123">INPUTS</span></span>

### <span data-ttu-id="7e791-124">않아야</span><span class="sxs-lookup"><span data-stu-id="7e791-124">None</span></span>

## <span data-ttu-id="7e791-125">출력</span><span class="sxs-lookup"><span data-stu-id="7e791-125">OUTPUTS</span></span>

### <span data-ttu-id="7e791-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="7e791-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e791-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7e791-127">NOTES</span></span>

## <span data-ttu-id="7e791-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e791-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e791-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e791-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="7e791-130">제거-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e791-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)

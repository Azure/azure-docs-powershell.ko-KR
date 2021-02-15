---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203641"
---
# <span data-ttu-id="67a1a-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="67a1a-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="67a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="67a1a-103">미디어 서비스 cmdlet에 대한 저장소 계정 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="67a1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="67a1a-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a1a-105">설명</span><span class="sxs-lookup"><span data-stu-id="67a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="67a1a-106">**New-AzMediaServiceStorageConfig** cmdlet은 미디어 서비스 cmdlet에 대한 저장소 계정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="67a1a-107">예제</span><span class="sxs-lookup"><span data-stu-id="67a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="67a1a-108">예제 1: 미디어 서비스 cmdlet에 대한 저장소 계정 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="67a1a-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="67a1a-109">첫 번째 명령은 **New-AzStorageAccount** cmdlet을 사용하여 저장소 계정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="67a1a-110">이 명령은 이 스토리지 계정 Storage1의 이름을 지정하고 형식은 Standard_GRS 이름이 지정되어 해당 저장소라는 변수에 $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="67a1a-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="67a1a-111">두 번째 명령은 저장소 변수에 저장된 저장소 계정 ID 정보를 사용하여 미디어 서비스에 연결된 기본 저장소 계정으로 저장소 구성 개체를 $StorageAccount 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="67a1a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a1a-112">PARAMETERS</span></span>

### <span data-ttu-id="67a1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a1a-113">-DefaultProfile</span></span>
<span data-ttu-id="67a1a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67a1a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67a1a-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="67a1a-115">-IsPrimary</span></span>
<span data-ttu-id="67a1a-116">cmdlet이 미디어 서비스의 기본 저장소로 저장소 계정을 만드는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a1a-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="67a1a-117">-StorageAccountId</span></span>
<span data-ttu-id="67a1a-118">저장소 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="67a1a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67a1a-119">-Confirm</span></span>
<span data-ttu-id="67a1a-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a1a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a1a-121">-WhatIf</span></span>
<span data-ttu-id="67a1a-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="67a1a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a1a-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a1a-124">CommonParameters</span></span>
<span data-ttu-id="67a1a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67a1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a1a-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67a1a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a1a-127">입력</span><span class="sxs-lookup"><span data-stu-id="67a1a-127">INPUTS</span></span>

### <span data-ttu-id="67a1a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67a1a-128">System.String</span></span>

## <span data-ttu-id="67a1a-129">출력</span><span class="sxs-lookup"><span data-stu-id="67a1a-129">OUTPUTS</span></span>

### <span data-ttu-id="67a1a-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67a1a-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="67a1a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67a1a-131">NOTES</span></span>

## <span data-ttu-id="67a1a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67a1a-132">RELATED LINKS</span></span>

[<span data-ttu-id="67a1a-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="67a1a-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)



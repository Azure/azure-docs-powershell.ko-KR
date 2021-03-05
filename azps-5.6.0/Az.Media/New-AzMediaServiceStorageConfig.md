---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 601b0bd8ff85ac3a89b3f07c3cf6e003c8005478
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006608"
---
# <span data-ttu-id="8e7fa-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="8e7fa-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="8e7fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7fa-103">미디어 서비스 cmdlet에 대한 저장소 계정 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="8e7fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e7fa-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7fa-106">**New-AzMediaServiceStorageConfig** cmdlet은 미디어 서비스 cmdlet에 대한 저장소 계정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="8e7fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="8e7fa-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7fa-108">예제 1: 미디어 서비스 cmdlet에 대한 저장소 계정 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="8e7fa-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="8e7fa-109">첫 번째 명령은 **New-AzStorageAccount** cmdlet을 사용하여 저장소 계정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="8e7fa-110">명령은 이 저장소 계정 Storage1의 이름을 지정하고 형식은 Standard_GRS 이름을 지정하고 결과를 $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="8e7fa-111">두 번째 명령은 저장소 변수에 저장된 저장소 계정 ID 정보를 사용하여 미디어 서비스에 연결된 기본 저장소 계정으로 저장소 구성 개체를 $StorageAccount 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="8e7fa-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e7fa-112">PARAMETERS</span></span>

### <span data-ttu-id="8e7fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7fa-113">-DefaultProfile</span></span>
<span data-ttu-id="8e7fa-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e7fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e7fa-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="8e7fa-115">-IsPrimary</span></span>
<span data-ttu-id="8e7fa-116">cmdlet이 미디어 서비스의 기본 저장소로 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="8e7fa-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e7fa-117">-StorageAccountId</span></span>
<span data-ttu-id="8e7fa-118">저장소 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="8e7fa-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8e7fa-119">-Confirm</span></span>
<span data-ttu-id="8e7fa-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7fa-121">-WhatIf</span></span>
<span data-ttu-id="8e7fa-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e7fa-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7fa-124">CommonParameters</span></span>
<span data-ttu-id="8e7fa-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7fa-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7fa-127">입력</span><span class="sxs-lookup"><span data-stu-id="8e7fa-127">INPUTS</span></span>

### <span data-ttu-id="8e7fa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8e7fa-128">System.String</span></span>

## <span data-ttu-id="8e7fa-129">출력</span><span class="sxs-lookup"><span data-stu-id="8e7fa-129">OUTPUTS</span></span>

### <span data-ttu-id="8e7fa-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e7fa-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="8e7fa-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e7fa-131">NOTES</span></span>

## <span data-ttu-id="8e7fa-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e7fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e7fa-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="8e7fa-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)



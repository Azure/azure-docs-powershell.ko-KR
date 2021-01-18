---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496747"
---
# <span data-ttu-id="95d82-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="95d82-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="95d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d82-102">SYNOPSIS</span></span>
<span data-ttu-id="95d82-103">미디어 서비스에 연결된 저장소 계정에 대한 저장소 계정 키를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="95d82-104">구문</span><span class="sxs-lookup"><span data-stu-id="95d82-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95d82-105">설명</span><span class="sxs-lookup"><span data-stu-id="95d82-105">DESCRIPTION</span></span>
<span data-ttu-id="95d82-106">**Sync-AzMediaServiceStorageKey** cmdlet은 미디어 서비스에 연결된 저장소 계정에 대한 저장소 계정 키를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="95d82-107">예제</span><span class="sxs-lookup"><span data-stu-id="95d82-107">EXAMPLES</span></span>

### <span data-ttu-id="95d82-108">예제 1: 미디어 서비스에 연결된 저장소 계정에 대한 저장소 계정 키 동기화</span><span class="sxs-lookup"><span data-stu-id="95d82-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="95d82-109">첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용하여 ResourceGroup001에 속하는 Storage135라는 저장소 계정을 구하고 결과를 $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="95d82-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="95d82-110">두 번째 명령은 mediaService001이라는 미디어 서비스에 대한 저장소  계정 키를 $StorageAccount 변수에 포함된 ID 속성을 사용하여 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="95d82-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d82-111">PARAMETERS</span></span>

### <span data-ttu-id="95d82-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95d82-112">-AccountName</span></span>
<span data-ttu-id="95d82-113">이 cmdlet이 동기화하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d82-114">-DefaultProfile</span></span>
<span data-ttu-id="95d82-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95d82-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95d82-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d82-116">-ResourceGroupName</span></span>
<span data-ttu-id="95d82-117">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="95d82-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95d82-118">-StorageAccountId</span></span>
<span data-ttu-id="95d82-119">미디어 서비스 계정과 연결된 저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d82-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95d82-120">-Confirm</span></span>
<span data-ttu-id="95d82-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d82-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d82-122">-WhatIf</span></span>
<span data-ttu-id="95d82-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="95d82-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d82-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d82-125">CommonParameters</span></span>
<span data-ttu-id="95d82-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95d82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d82-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95d82-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d82-128">입력</span><span class="sxs-lookup"><span data-stu-id="95d82-128">INPUTS</span></span>

### <span data-ttu-id="95d82-129">System.String</span><span class="sxs-lookup"><span data-stu-id="95d82-129">System.String</span></span>

## <span data-ttu-id="95d82-130">출력</span><span class="sxs-lookup"><span data-stu-id="95d82-130">OUTPUTS</span></span>

### <span data-ttu-id="95d82-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95d82-131">System.Boolean</span></span>

## <span data-ttu-id="95d82-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95d82-132">NOTES</span></span>

## <span data-ttu-id="95d82-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d82-133">RELATED LINKS</span></span>

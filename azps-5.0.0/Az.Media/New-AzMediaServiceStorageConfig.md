---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226800"
---
# <span data-ttu-id="08c47-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="08c47-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="08c47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c47-102">SYNOPSIS</span></span>
<span data-ttu-id="08c47-103">미디어 서비스 cmdlet에 대 한 저장소 계정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="08c47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08c47-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c47-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08c47-105">DESCRIPTION</span></span>
<span data-ttu-id="08c47-106">**AzMediaServiceStorageConfig** cmdlet은 미디어 서비스 cmdlet에 대 한 저장소 계정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="08c47-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08c47-107">EXAMPLES</span></span>

### <span data-ttu-id="08c47-108">예제 1: 미디어 서비스 cmdlet에 대 한 저장소 계정 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="08c47-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="08c47-109">첫 번째 명령은 **New AzStorageAccount cmdlet을** 사용 하 여 저장소 계정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="08c47-110">이 저장소 계정의 이름 Storage1와 형식이 Standard_GRS으로 지정 되 고 그 결과가 $StorageAccount 이라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="08c47-111">두 번째 명령은 $StorageAccount 변수에 저장 된 저장소 계정 ID 정보를 사용 하 여 미디어 서비스와 연결 된 기본 저장소 계정으로 저장소 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="08c47-112">변수</span><span class="sxs-lookup"><span data-stu-id="08c47-112">PARAMETERS</span></span>

### <span data-ttu-id="08c47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c47-113">-DefaultProfile</span></span>
<span data-ttu-id="08c47-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08c47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08c47-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="08c47-115">-IsPrimary</span></span>
<span data-ttu-id="08c47-116">Cmdlet이 미디어 서비스의 기본 저장소로 저장소 계정을 만드는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="08c47-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="08c47-117">-StorageAccountId</span></span>
<span data-ttu-id="08c47-118">저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="08c47-119">-확인</span><span class="sxs-lookup"><span data-stu-id="08c47-119">-Confirm</span></span>
<span data-ttu-id="08c47-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c47-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c47-121">-WhatIf</span></span>
<span data-ttu-id="08c47-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c47-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c47-124">CommonParameters</span></span>
<span data-ttu-id="08c47-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08c47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c47-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c47-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c47-127">입력</span><span class="sxs-lookup"><span data-stu-id="08c47-127">INPUTS</span></span>

### <span data-ttu-id="08c47-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08c47-128">System.String</span></span>

## <span data-ttu-id="08c47-129">출력</span><span class="sxs-lookup"><span data-stu-id="08c47-129">OUTPUTS</span></span>

### <span data-ttu-id="08c47-130">Microsoft. Azure. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08c47-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="08c47-131">상속자</span><span class="sxs-lookup"><span data-stu-id="08c47-131">NOTES</span></span>

## <span data-ttu-id="08c47-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08c47-132">RELATED LINKS</span></span>

[<span data-ttu-id="08c47-133">동기화-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="08c47-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)



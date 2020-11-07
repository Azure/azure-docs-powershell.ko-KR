---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: e9d413a8f77422b723c2dabc57d7d68c691617d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867397"
---
# <span data-ttu-id="0662f-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="0662f-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="0662f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0662f-102">SYNOPSIS</span></span>
<span data-ttu-id="0662f-103">미디어 서비스와 연결 된 저장소 계정에 대 한 저장소 계정 키를 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="0662f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0662f-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0662f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0662f-105">DESCRIPTION</span></span>
<span data-ttu-id="0662f-106">**동기화-AzMediaServiceStorageKey** cmdlet은 미디어 서비스와 연결 된 저장소 계정에 대 한 저장소 계정 키를 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="0662f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0662f-107">EXAMPLES</span></span>

### <span data-ttu-id="0662f-108">예제 1: 미디어 서비스와 연결 된 저장소 계정에 대해 저장소 계정 키 동기화</span><span class="sxs-lookup"><span data-stu-id="0662f-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="0662f-109">첫 번째 명령은 Get-AzStorageAccount cmdlet을 사용 하 여 ResourceGroup001에 속한 Storage135 이라는 저장소 계정을 가져오고 결과를 $StorageAccount 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="0662f-110">두 번째 명령은 $StorageAccount 변수에 포함 된 **Id** 속성을 사용 하 여 MediaService001 이라는 미디어 서비스에 대 한 저장소 계정 키를 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="0662f-111">변수</span><span class="sxs-lookup"><span data-stu-id="0662f-111">PARAMETERS</span></span>

### <span data-ttu-id="0662f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0662f-112">-AccountName</span></span>
<span data-ttu-id="0662f-113">이 cmdlet이 동기화 하는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="0662f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0662f-114">-DefaultProfile</span></span>
<span data-ttu-id="0662f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0662f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0662f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0662f-116">-ResourceGroupName</span></span>
<span data-ttu-id="0662f-117">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="0662f-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0662f-118">-StorageAccountId</span></span>
<span data-ttu-id="0662f-119">미디어 서비스 계정과 연결 된 저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="0662f-120">-확인</span><span class="sxs-lookup"><span data-stu-id="0662f-120">-Confirm</span></span>
<span data-ttu-id="0662f-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0662f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0662f-122">-WhatIf</span></span>
<span data-ttu-id="0662f-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0662f-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0662f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0662f-125">CommonParameters</span></span>
<span data-ttu-id="0662f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0662f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0662f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0662f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0662f-128">입력</span><span class="sxs-lookup"><span data-stu-id="0662f-128">INPUTS</span></span>

### <span data-ttu-id="0662f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0662f-129">System.String</span></span>

## <span data-ttu-id="0662f-130">출력</span><span class="sxs-lookup"><span data-stu-id="0662f-130">OUTPUTS</span></span>

### <span data-ttu-id="0662f-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0662f-131">System.Boolean</span></span>

## <span data-ttu-id="0662f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0662f-132">NOTES</span></span>

## <span data-ttu-id="0662f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0662f-133">RELATED LINKS</span></span>

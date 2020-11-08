---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045678"
---
# <span data-ttu-id="851de-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="851de-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="851de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851de-102">SYNOPSIS</span></span>
<span data-ttu-id="851de-103">하나의 Azure RemoteApp 컬렉션에서 지정 된 Azure 저장소 계정으로 모든 사용자 디스크를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="851de-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="851de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="851de-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="851de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="851de-105">DESCRIPTION</span></span>
<span data-ttu-id="851de-106">**AzureRemoteAppUserDisk** cmdlet은 하나의 azure RemoteApp 컬렉션에서 지정 된 azure 저장소 계정으로 모든 사용자 디스크를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="851de-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="851de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="851de-107">EXAMPLES</span></span>

### <span data-ttu-id="851de-108">예제 1: 컬렉션의 모든 사용자 디스크를 지정 된 Azure 저장소 계정으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="851de-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="851de-109">이 명령은 Contoso 라는 컬렉션의 모든 사용자 디스크를 지정 된 Azure storage 계정에서 이름 AccountName 및 키 AccountKey 인 ContainerName 이라는 컨테이너로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="851de-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="851de-110">변수</span><span class="sxs-lookup"><span data-stu-id="851de-110">PARAMETERS</span></span>

### <span data-ttu-id="851de-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="851de-111">-CollectionName</span></span>
<span data-ttu-id="851de-112">원본 Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851de-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="851de-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="851de-114">대상 Azure 저장소 계정에서 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851de-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="851de-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="851de-116">대상 Azure 저장소 계정의 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-116">Specifies the Key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851de-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="851de-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="851de-118">대상 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851de-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="851de-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="851de-120">Cmdlet이 기존 사용자 디스크를 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="851de-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851de-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="851de-121">-Profile</span></span>
<span data-ttu-id="851de-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="851de-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="851de-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851de-124">-확인</span><span class="sxs-lookup"><span data-stu-id="851de-124">-Confirm</span></span>
<span data-ttu-id="851de-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="851de-126">-WhatIf</span></span>
<span data-ttu-id="851de-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="851de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="851de-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="851de-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851de-129">CommonParameters</span></span>
<span data-ttu-id="851de-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="851de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851de-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851de-132">입력</span><span class="sxs-lookup"><span data-stu-id="851de-132">INPUTS</span></span>

## <span data-ttu-id="851de-133">출력</span><span class="sxs-lookup"><span data-stu-id="851de-133">OUTPUTS</span></span>

## <span data-ttu-id="851de-134">상속자</span><span class="sxs-lookup"><span data-stu-id="851de-134">NOTES</span></span>

## <span data-ttu-id="851de-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="851de-135">RELATED LINKS</span></span>

[<span data-ttu-id="851de-136">복사-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="851de-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="851de-137">제거-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="851de-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)



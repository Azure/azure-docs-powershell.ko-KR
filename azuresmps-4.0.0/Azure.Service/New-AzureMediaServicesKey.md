---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046001"
---
# <span data-ttu-id="f89a1-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="f89a1-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="f89a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f89a1-103">Azure 미디어 서비스 계정 키를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="f89a1-104">**참고:** 이 버전은 더 이상 사용 되지 않습니다. [최신 버전](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="f89a1-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="f89a1-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f89a1-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f89a1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f89a1-106">DESCRIPTION</span></span>
<span data-ttu-id="f89a1-107">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f89a1-108">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f89a1-109">**AzureMediaServicesKey** cmdlet은 지정 된 미디어 서비스 계정에 대 한 기본 또는 보조 키를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="f89a1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f89a1-110">EXAMPLES</span></span>

### <span data-ttu-id="f89a1-111">예제 1: Media Services 계정 키 업데이트</span><span class="sxs-lookup"><span data-stu-id="f89a1-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="f89a1-112">변수</span><span class="sxs-lookup"><span data-stu-id="f89a1-112">PARAMETERS</span></span>

### <span data-ttu-id="f89a1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f89a1-113">-Force</span></span>
<span data-ttu-id="f89a1-114">키 생성이 확인 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-114">Indicates that the key generation is not confirmed.</span></span>

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

### <span data-ttu-id="f89a1-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f89a1-115">-KeyType</span></span>
<span data-ttu-id="f89a1-116">미디어 서비스 키 종류를 지정 합니다. 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="f89a1-117">주요한</span><span class="sxs-lookup"><span data-stu-id="f89a1-117">Primary</span></span>
- <span data-ttu-id="f89a1-118">보조</span><span class="sxs-lookup"><span data-stu-id="f89a1-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89a1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f89a1-119">-Name</span></span>
<span data-ttu-id="f89a1-120">미디어 서비스 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-120">Specifies the name of the Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89a1-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="f89a1-121">-Profile</span></span>
<span data-ttu-id="f89a1-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f89a1-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f89a1-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f89a1-124">-Confirm</span></span>
<span data-ttu-id="f89a1-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f89a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89a1-126">-WhatIf</span></span>
<span data-ttu-id="f89a1-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f89a1-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f89a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89a1-129">CommonParameters</span></span>
<span data-ttu-id="f89a1-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89a1-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89a1-132">입력</span><span class="sxs-lookup"><span data-stu-id="f89a1-132">INPUTS</span></span>

## <span data-ttu-id="f89a1-133">출력</span><span class="sxs-lookup"><span data-stu-id="f89a1-133">OUTPUTS</span></span>

## <span data-ttu-id="f89a1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f89a1-134">NOTES</span></span>

## <span data-ttu-id="f89a1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f89a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="f89a1-136">미디어 서비스에 Azure PowerShell을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f89a1-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)



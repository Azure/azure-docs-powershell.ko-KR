---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046471"
---
# <span data-ttu-id="51319-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="51319-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="51319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51319-102">SYNOPSIS</span></span>
<span data-ttu-id="51319-103">지정 된 Azure Media 서비스 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="51319-104">**참고:**  이 버전은 더 이상 사용 되지 않습니다. [최신 버전](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="51319-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="51319-105">구문과</span><span class="sxs-lookup"><span data-stu-id="51319-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51319-106">설명은</span><span class="sxs-lookup"><span data-stu-id="51319-106">DESCRIPTION</span></span>
<span data-ttu-id="51319-107">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51319-108">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51319-109">**AzureMediaServicesAccount** Cmdlet은 미디어 서비스 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="51319-110">예제의</span><span class="sxs-lookup"><span data-stu-id="51319-110">EXAMPLES</span></span>

### <span data-ttu-id="51319-111">예제 1: 미디어 서비스 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="51319-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="51319-112">변수</span><span class="sxs-lookup"><span data-stu-id="51319-112">PARAMETERS</span></span>

### <span data-ttu-id="51319-113">-Force</span><span class="sxs-lookup"><span data-stu-id="51319-113">-Force</span></span>
<span data-ttu-id="51319-114">*Force* 스위치를 지정 하면 삭제가 확인 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51319-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="51319-115">-이름</span><span class="sxs-lookup"><span data-stu-id="51319-115">-Name</span></span>
<span data-ttu-id="51319-116">미디어 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51319-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="51319-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="51319-117">-Profile</span></span>
<span data-ttu-id="51319-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51319-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="51319-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51319-120">-확인</span><span class="sxs-lookup"><span data-stu-id="51319-120">-Confirm</span></span>
<span data-ttu-id="51319-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51319-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51319-122">-WhatIf</span></span>
<span data-ttu-id="51319-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51319-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51319-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51319-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51319-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51319-125">CommonParameters</span></span>
<span data-ttu-id="51319-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51319-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51319-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51319-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51319-128">입력</span><span class="sxs-lookup"><span data-stu-id="51319-128">INPUTS</span></span>

## <span data-ttu-id="51319-129">출력</span><span class="sxs-lookup"><span data-stu-id="51319-129">OUTPUTS</span></span>

## <span data-ttu-id="51319-130">상속자</span><span class="sxs-lookup"><span data-stu-id="51319-130">NOTES</span></span>

## <span data-ttu-id="51319-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51319-131">RELATED LINKS</span></span>

[<span data-ttu-id="51319-132">미디어 서비스에 Azure PowerShell을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="51319-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="51319-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="51319-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="51319-134">새로운 AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="51319-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)



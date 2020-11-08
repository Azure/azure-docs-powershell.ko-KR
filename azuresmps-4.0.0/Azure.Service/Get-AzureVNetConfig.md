---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046288"
---
# <span data-ttu-id="c9e98-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="c9e98-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="c9e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e98-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e98-103">현재 구독에서 Azure 가상 네트워크 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="c9e98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9e98-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9e98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9e98-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e98-106">**Get-AzureVNetConfig** cmdlet은 현재 Azure 구독에 대 한 가상 네트워크 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="c9e98-107">*Exporttofile* 매개 변수를 지정 하면 네트워크 구성 파일이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="c9e98-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c9e98-108">EXAMPLES</span></span>

### <span data-ttu-id="c9e98-109">예제 1: 현재 Azure 구독에 대 한 가상 네트워크 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9e98-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="c9e98-110">이 명령은 현재 Azure 구독에 대 한 가상 네트워크 구성을 가져와 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="c9e98-111">예제 2: 현재 Azure 구독에 대 한 가상 네트워크 구성을 가져오고 로컬 파일에 저장</span><span class="sxs-lookup"><span data-stu-id="c9e98-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="c9e98-112">이 명령은 현재 Azure 구독에 대 한 가상 네트워크 구성을 가져온 다음 로컬 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="c9e98-113">변수</span><span class="sxs-lookup"><span data-stu-id="c9e98-113">PARAMETERS</span></span>

### <span data-ttu-id="c9e98-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="c9e98-114">-ExportToFile</span></span>
<span data-ttu-id="c9e98-115">설정에서 만들 네트워크 구성 파일의 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e98-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9e98-116">-InformationAction</span></span>
<span data-ttu-id="c9e98-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9e98-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9e98-119">하기로</span><span class="sxs-lookup"><span data-stu-id="c9e98-119">Continue</span></span>
- <span data-ttu-id="c9e98-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="c9e98-120">Ignore</span></span>
- <span data-ttu-id="c9e98-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="c9e98-121">Inquire</span></span>
- <span data-ttu-id="c9e98-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9e98-122">SilentlyContinue</span></span>
- <span data-ttu-id="c9e98-123">중지가</span><span class="sxs-lookup"><span data-stu-id="c9e98-123">Stop</span></span>
- <span data-ttu-id="c9e98-124">대기</span><span class="sxs-lookup"><span data-stu-id="c9e98-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e98-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9e98-125">-InformationVariable</span></span>
<span data-ttu-id="c9e98-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e98-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="c9e98-127">-Profile</span></span>
<span data-ttu-id="c9e98-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9e98-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9e98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e98-130">CommonParameters</span></span>
<span data-ttu-id="c9e98-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9e98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e98-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e98-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e98-133">입력</span><span class="sxs-lookup"><span data-stu-id="c9e98-133">INPUTS</span></span>

## <span data-ttu-id="c9e98-134">출력</span><span class="sxs-lookup"><span data-stu-id="c9e98-134">OUTPUTS</span></span>

## <span data-ttu-id="c9e98-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c9e98-135">NOTES</span></span>

## <span data-ttu-id="c9e98-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9e98-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9e98-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="c9e98-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="c9e98-138">-AzureVNetConfig 제거</span><span class="sxs-lookup"><span data-stu-id="c9e98-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="c9e98-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="c9e98-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)



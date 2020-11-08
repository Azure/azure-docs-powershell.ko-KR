---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045690"
---
# <span data-ttu-id="2789a-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2789a-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="2789a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2789a-102">SYNOPSIS</span></span>
<span data-ttu-id="2789a-103">Azure 웹 사이트에 대 한 application diagnostics를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="2789a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2789a-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2789a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2789a-105">DESCRIPTION</span></span>
<span data-ttu-id="2789a-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2789a-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2789a-108">Azure 웹 사이트에 대 한 application diagnostics를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="2789a-109">파일 시스템 또는 Azure에 저장 되도록 구성 된 로깅을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="2789a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2789a-110">EXAMPLES</span></span>

### <span data-ttu-id="2789a-111">예제 1: 응용 프로그램 로깅 파일 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2789a-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="2789a-112">다음 예제에서는 파일 시스템에서 응용 프로그램 로깅을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="2789a-113">예제 2: Azure storage를 사용 하 여 로깅 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2789a-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="2789a-114">다음 예제에서는 저장소를 사용 하 여 응용 프로그램 로깅을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="2789a-115">변수</span><span class="sxs-lookup"><span data-stu-id="2789a-115">PARAMETERS</span></span>

### <span data-ttu-id="2789a-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="2789a-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2789a-117">-파일</span><span class="sxs-lookup"><span data-stu-id="2789a-117">-File</span></span>
<span data-ttu-id="2789a-118">파일 시스템을 사용 하 여 로그 파일을 저장할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2789a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2789a-119">-Name</span></span>
<span data-ttu-id="2789a-120">웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-120">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2789a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2789a-121">-PassThru</span></span>
<span data-ttu-id="2789a-122">성공한 경우 true를 반환 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="2789a-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="2789a-123">-Profile</span></span>
<span data-ttu-id="2789a-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2789a-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2789a-126">-슬롯</span><span class="sxs-lookup"><span data-stu-id="2789a-126">-Slot</span></span>
<span data-ttu-id="2789a-127">슬롯의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-127">Specifies the name of slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2789a-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="2789a-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2789a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2789a-129">CommonParameters</span></span>
<span data-ttu-id="2789a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2789a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2789a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2789a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2789a-132">입력</span><span class="sxs-lookup"><span data-stu-id="2789a-132">INPUTS</span></span>

## <span data-ttu-id="2789a-133">출력</span><span class="sxs-lookup"><span data-stu-id="2789a-133">OUTPUTS</span></span>

## <span data-ttu-id="2789a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2789a-134">NOTES</span></span>

## <span data-ttu-id="2789a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2789a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2789a-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2789a-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="2789a-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2789a-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2789a-138">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2789a-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2789a-139">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2789a-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2789a-140">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2789a-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)



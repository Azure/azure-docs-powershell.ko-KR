---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045830"
---
# <span data-ttu-id="fa9f7-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa9f7-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="fa9f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9f7-102">SYNOPSIS</span></span>

<span data-ttu-id="fa9f7-103">자동화에서 모듈을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="fa9f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa9f7-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa9f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa9f7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="fa9f7-106">**Set AzureAutomationModule** cmdlet은 모듈의 새 버전을 가져오거나 Azure Automation에서 모듈의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="fa9f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa9f7-107">EXAMPLES</span></span>

### <span data-ttu-id="fa9f7-108">예제 1: 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="fa9f7-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="fa9f7-109">이 명령은 ContosoModule 이라는 기존 모듈의 업데이트 된 버전을 Contoso17 라는 Azure Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fa9f7-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa9f7-110">PARAMETERS</span></span>

### <span data-ttu-id="fa9f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fa9f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="fa9f7-112">모듈과 함께 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="fa9f7-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="fa9f7-113">-ContentLinkUri</span></span>
<span data-ttu-id="fa9f7-114">모듈 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f7-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="fa9f7-115">-ContentLinkVersion</span></span>
<span data-ttu-id="fa9f7-116">모듈의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="fa9f7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fa9f7-117">-Name</span></span>
<span data-ttu-id="fa9f7-118">모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="fa9f7-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="fa9f7-119">-Profile</span></span>
<span data-ttu-id="fa9f7-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa9f7-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa9f7-122">태그</span><span class="sxs-lookup"><span data-stu-id="fa9f7-122">-Tags</span></span>
<span data-ttu-id="fa9f7-123">모듈에 대 한 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9f7-124">CommonParameters</span></span>
<span data-ttu-id="fa9f7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9f7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9f7-127">입력</span><span class="sxs-lookup"><span data-stu-id="fa9f7-127">INPUTS</span></span>

### <span data-ttu-id="fa9f7-128">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="fa9f7-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="fa9f7-129">출력</span><span class="sxs-lookup"><span data-stu-id="fa9f7-129">OUTPUTS</span></span>

## <span data-ttu-id="fa9f7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fa9f7-130">NOTES</span></span>

## <span data-ttu-id="fa9f7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa9f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="fa9f7-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa9f7-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="fa9f7-133">새-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fa9f7-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="fa9f7-134">-AzureAutomationModule 제거</span><span class="sxs-lookup"><span data-stu-id="fa9f7-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)



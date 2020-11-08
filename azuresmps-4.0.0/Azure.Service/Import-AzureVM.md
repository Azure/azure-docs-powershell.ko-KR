---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046255"
---
# <span data-ttu-id="f20c2-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f20c2-101">Import-AzureVM</span></span>

## <span data-ttu-id="f20c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f20c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f20c2-103">파일에서 Azure 가상 컴퓨터 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="f20c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f20c2-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f20c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f20c2-105">DESCRIPTION</span></span>
<span data-ttu-id="f20c2-106">**가져오기-add-azurevm** cmdlet은 이전에 저장 된 가상 컴퓨터의 상태를 XML 파일에서 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="f20c2-107">이 cmdlet은 가져온 데이터에서 가상 컴퓨터를 만들 때 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="f20c2-108">**Export-** a 2를 실행 하 고 **제거한** 후에는 **-** add-azurevm를 가져와 가상 컴퓨터를 다시 만들면 결과 가상 컴퓨터의 IP 주소가 원본과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="f20c2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f20c2-109">EXAMPLES</span></span>

### <span data-ttu-id="f20c2-110">예제 1: 가상 컴퓨터 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="f20c2-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="f20c2-111">이 명령은 VMstate.xml 파일에서 가상 컴퓨터의 상태를 가져온 다음 지정 된 클라우드 서비스에서 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="f20c2-112">변수</span><span class="sxs-lookup"><span data-stu-id="f20c2-112">PARAMETERS</span></span>

### <span data-ttu-id="f20c2-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f20c2-113">-InformationAction</span></span>
<span data-ttu-id="f20c2-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f20c2-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f20c2-116">하기로</span><span class="sxs-lookup"><span data-stu-id="f20c2-116">Continue</span></span>
- <span data-ttu-id="f20c2-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="f20c2-117">Ignore</span></span>
- <span data-ttu-id="f20c2-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="f20c2-118">Inquire</span></span>
- <span data-ttu-id="f20c2-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f20c2-119">SilentlyContinue</span></span>
- <span data-ttu-id="f20c2-120">중지가</span><span class="sxs-lookup"><span data-stu-id="f20c2-120">Stop</span></span>
- <span data-ttu-id="f20c2-121">대기</span><span class="sxs-lookup"><span data-stu-id="f20c2-121">Suspend</span></span>

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

### <span data-ttu-id="f20c2-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f20c2-122">-InformationVariable</span></span>
<span data-ttu-id="f20c2-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f20c2-124">-Path</span><span class="sxs-lookup"><span data-stu-id="f20c2-124">-Path</span></span>
<span data-ttu-id="f20c2-125">이전에 저장 된 가상 컴퓨터 상태를 사용 하 여 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20c2-126">CommonParameters</span></span>
<span data-ttu-id="f20c2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20c2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f20c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20c2-129">입력</span><span class="sxs-lookup"><span data-stu-id="f20c2-129">INPUTS</span></span>

## <span data-ttu-id="f20c2-130">출력</span><span class="sxs-lookup"><span data-stu-id="f20c2-130">OUTPUTS</span></span>

## <span data-ttu-id="f20c2-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f20c2-131">NOTES</span></span>

## <span data-ttu-id="f20c2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f20c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="f20c2-133">수출-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f20c2-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="f20c2-134">뉴욕</span><span class="sxs-lookup"><span data-stu-id="f20c2-134">New-AzureVM</span></span>](./New-AzureVM.md)



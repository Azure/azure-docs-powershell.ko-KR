---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045645"
---
# <span data-ttu-id="a1391-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1391-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="a1391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1391-102">SYNOPSIS</span></span>
<span data-ttu-id="a1391-103">Azure 가상 컴퓨터에 할당 된 끝점에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="a1391-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1391-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a1391-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1391-105">DESCRIPTION</span></span>
<span data-ttu-id="a1391-106">**Get-AzureEndpoint** Cmdlet은 Azure 가상 컴퓨터에 할당 된 끝점에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="a1391-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a1391-107">EXAMPLES</span></span>

### <span data-ttu-id="a1391-108">예제 1: 가상 컴퓨터에 대 한 끝점 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1391-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="a1391-109">이 명령은 **get-help** cmdlet을 사용 하 여 VirtualMachine12 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a1391-110">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a1391-111">이 cmdlet은 해당 가상 컴퓨터에 대 한 끝점 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="a1391-112">변수</span><span class="sxs-lookup"><span data-stu-id="a1391-112">PARAMETERS</span></span>

### <span data-ttu-id="a1391-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a1391-113">-InformationAction</span></span>
<span data-ttu-id="a1391-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a1391-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1391-116">하기로</span><span class="sxs-lookup"><span data-stu-id="a1391-116">Continue</span></span>
- <span data-ttu-id="a1391-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="a1391-117">Ignore</span></span>
- <span data-ttu-id="a1391-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="a1391-118">Inquire</span></span>
- <span data-ttu-id="a1391-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a1391-119">SilentlyContinue</span></span>
- <span data-ttu-id="a1391-120">중지가</span><span class="sxs-lookup"><span data-stu-id="a1391-120">Stop</span></span>
- <span data-ttu-id="a1391-121">대기</span><span class="sxs-lookup"><span data-stu-id="a1391-121">Suspend</span></span>

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

### <span data-ttu-id="a1391-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a1391-122">-InformationVariable</span></span>
<span data-ttu-id="a1391-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a1391-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a1391-124">-Name</span></span>
<span data-ttu-id="a1391-125">이 cmdlet에서 정보를 가져오는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1391-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="a1391-126">-Profile</span></span>
<span data-ttu-id="a1391-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1391-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1391-129">-VM</span><span class="sxs-lookup"><span data-stu-id="a1391-129">-VM</span></span>
<span data-ttu-id="a1391-130">이 cmdlet이 끝점 정보를 가져오는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1391-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1391-131">CommonParameters</span></span>
<span data-ttu-id="a1391-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1391-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1391-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1391-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1391-134">입력</span><span class="sxs-lookup"><span data-stu-id="a1391-134">INPUTS</span></span>

## <span data-ttu-id="a1391-135">출력</span><span class="sxs-lookup"><span data-stu-id="a1391-135">OUTPUTS</span></span>

## <span data-ttu-id="a1391-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a1391-136">NOTES</span></span>

## <span data-ttu-id="a1391-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1391-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1391-138">추가-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1391-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="a1391-139">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a1391-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a1391-140">-AzureEndpoint 제거</span><span class="sxs-lookup"><span data-stu-id="a1391-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="a1391-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1391-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)



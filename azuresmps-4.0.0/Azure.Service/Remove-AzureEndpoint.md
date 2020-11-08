---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046478"
---
# <span data-ttu-id="6ed4d-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ed4d-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="6ed4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed4d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed4d-103">Azure 가상 머신에서 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="6ed4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ed4d-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ed4d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6ed4d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed4d-106">**제거-azureendpoint** Cmdlet은 Azure 가상 머신 개체에서 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="6ed4d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6ed4d-107">EXAMPLES</span></span>

### <span data-ttu-id="6ed4d-108">예제 1: 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="6ed4d-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="6ed4d-109">이 명령은 **get-help** cmdlet을 사용 하 여 VirtualMachine01 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="6ed4d-110">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ed4d-111">이 cmdlet은 HttpIn 이라는 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="6ed4d-112">이 명령은 가상 컴퓨터 개체를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="6ed4d-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ed4d-113">PARAMETERS</span></span>

### <span data-ttu-id="6ed4d-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ed4d-114">-InformationAction</span></span>
<span data-ttu-id="6ed4d-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ed4d-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ed4d-117">하기로</span><span class="sxs-lookup"><span data-stu-id="6ed4d-117">Continue</span></span>
- <span data-ttu-id="6ed4d-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="6ed4d-118">Ignore</span></span>
- <span data-ttu-id="6ed4d-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="6ed4d-119">Inquire</span></span>
- <span data-ttu-id="6ed4d-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ed4d-120">SilentlyContinue</span></span>
- <span data-ttu-id="6ed4d-121">중지가</span><span class="sxs-lookup"><span data-stu-id="6ed4d-121">Stop</span></span>
- <span data-ttu-id="6ed4d-122">대기</span><span class="sxs-lookup"><span data-stu-id="6ed4d-122">Suspend</span></span>

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

### <span data-ttu-id="6ed4d-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ed4d-123">-InformationVariable</span></span>
<span data-ttu-id="6ed4d-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ed4d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6ed4d-125">-Name</span></span>
<span data-ttu-id="6ed4d-126">이 cmdlet이 가상 컴퓨터에서 삭제 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="6ed4d-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="6ed4d-127">-Profile</span></span>
<span data-ttu-id="6ed4d-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ed4d-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ed4d-130">-VM</span><span class="sxs-lookup"><span data-stu-id="6ed4d-130">-VM</span></span>
<span data-ttu-id="6ed4d-131">이 cmdlet이 끝점을 삭제 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="6ed4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed4d-132">CommonParameters</span></span>
<span data-ttu-id="6ed4d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed4d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ed4d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed4d-135">입력</span><span class="sxs-lookup"><span data-stu-id="6ed4d-135">INPUTS</span></span>

## <span data-ttu-id="6ed4d-136">출력</span><span class="sxs-lookup"><span data-stu-id="6ed4d-136">OUTPUTS</span></span>

## <span data-ttu-id="6ed4d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6ed4d-137">NOTES</span></span>

## <span data-ttu-id="6ed4d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ed4d-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ed4d-139">추가-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ed4d-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="6ed4d-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ed4d-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="6ed4d-141">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ed4d-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6ed4d-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ed4d-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="6ed4d-143">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6ed4d-143">Update-AzureVM</span></span>](./Update-AzureVM.md)



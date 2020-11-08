---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045771"
---
# <span data-ttu-id="d3380-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d3380-101">Start-AzureVM</span></span>

## <span data-ttu-id="d3380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3380-102">SYNOPSIS</span></span>
<span data-ttu-id="d3380-103">Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="d3380-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3380-104">SYNTAX</span></span>

### <span data-ttu-id="d3380-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3380-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3380-106">의견</span><span class="sxs-lookup"><span data-stu-id="d3380-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d3380-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d3380-107">DESCRIPTION</span></span>
<span data-ttu-id="d3380-108">**시작-add-azurevm** Cmdlet은 Azure 가상 컴퓨터의 시작을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="d3380-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d3380-109">EXAMPLES</span></span>

### <span data-ttu-id="d3380-110">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="d3380-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="d3380-111">이 명령은 ContosoService03 이라는 Azure 서비스에서 실행 되는 VirtualMachine04 이라는 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="d3380-112">예제 2: 가상 컴퓨터 개체를 사용 하 여 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="d3380-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="d3380-113">이 명령은 이름이 DatabaseServer 인 가상 컴퓨터의 가상 컴퓨터 개체를 검색 한 다음 시작 하도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="d3380-114">변수</span><span class="sxs-lookup"><span data-stu-id="d3380-114">PARAMETERS</span></span>

### <span data-ttu-id="d3380-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d3380-115">-InformationAction</span></span>
<span data-ttu-id="d3380-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d3380-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3380-118">하기로</span><span class="sxs-lookup"><span data-stu-id="d3380-118">Continue</span></span>
- <span data-ttu-id="d3380-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="d3380-119">Ignore</span></span>
- <span data-ttu-id="d3380-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="d3380-120">Inquire</span></span>
- <span data-ttu-id="d3380-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d3380-121">SilentlyContinue</span></span>
- <span data-ttu-id="d3380-122">중지가</span><span class="sxs-lookup"><span data-stu-id="d3380-122">Stop</span></span>
- <span data-ttu-id="d3380-123">대기</span><span class="sxs-lookup"><span data-stu-id="d3380-123">Suspend</span></span>

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

### <span data-ttu-id="d3380-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d3380-124">-InformationVariable</span></span>
<span data-ttu-id="d3380-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d3380-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d3380-126">-Name</span></span>
<span data-ttu-id="d3380-127">시작할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3380-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="d3380-128">-Profile</span></span>
<span data-ttu-id="d3380-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3380-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3380-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d3380-131">-ServiceName</span></span>
<span data-ttu-id="d3380-132">시작할 가상 컴퓨터를 포함 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3380-133">-VM</span><span class="sxs-lookup"><span data-stu-id="d3380-133">-VM</span></span>
<span data-ttu-id="d3380-134">시작할 가상 컴퓨터를 식별 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3380-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3380-135">CommonParameters</span></span>
<span data-ttu-id="d3380-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3380-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3380-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3380-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3380-138">입력</span><span class="sxs-lookup"><span data-stu-id="d3380-138">INPUTS</span></span>

## <span data-ttu-id="d3380-139">출력</span><span class="sxs-lookup"><span data-stu-id="d3380-139">OUTPUTS</span></span>

## <span data-ttu-id="d3380-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d3380-140">NOTES</span></span>

## <span data-ttu-id="d3380-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3380-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3380-142">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d3380-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d3380-143">제거-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d3380-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="d3380-144">-Add-azurevm 다시 시작</span><span class="sxs-lookup"><span data-stu-id="d3380-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="d3380-145">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d3380-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="d3380-146">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d3380-146">Update-AzureVM</span></span>](./Update-AzureVM.md)



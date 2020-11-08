---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045677"
---
# <span data-ttu-id="45d80-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="45d80-101">Export-AzureVM</span></span>

## <span data-ttu-id="45d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d80-102">SYNOPSIS</span></span>
<span data-ttu-id="45d80-103">Azure 가상 컴퓨터 상태를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="45d80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45d80-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="45d80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45d80-105">DESCRIPTION</span></span>
<span data-ttu-id="45d80-106">**Export-add-azurevm** cmdlet은 가상 컴퓨터의 상태를 .xml 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="45d80-107">**Export-** a 2를 실행 하 고 **제거한** 후에는 **-** add-azurevm를 가져와 가상 컴퓨터를 다시 만들면 결과 가상 컴퓨터의 IP 주소가 원본과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="45d80-108">예제의</span><span class="sxs-lookup"><span data-stu-id="45d80-108">EXAMPLES</span></span>

### <span data-ttu-id="45d80-109">예제 1: 가상 컴퓨터 내보내기</span><span class="sxs-lookup"><span data-stu-id="45d80-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="45d80-110">이 명령은 지정 된 가상 컴퓨터의 상태를 VMstate.xml 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="45d80-111">변수</span><span class="sxs-lookup"><span data-stu-id="45d80-111">PARAMETERS</span></span>

### <span data-ttu-id="45d80-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="45d80-112">-InformationAction</span></span>
<span data-ttu-id="45d80-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="45d80-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45d80-115">하기로</span><span class="sxs-lookup"><span data-stu-id="45d80-115">Continue</span></span>
- <span data-ttu-id="45d80-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="45d80-116">Ignore</span></span>
- <span data-ttu-id="45d80-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="45d80-117">Inquire</span></span>
- <span data-ttu-id="45d80-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="45d80-118">SilentlyContinue</span></span>
- <span data-ttu-id="45d80-119">중지가</span><span class="sxs-lookup"><span data-stu-id="45d80-119">Stop</span></span>
- <span data-ttu-id="45d80-120">대기</span><span class="sxs-lookup"><span data-stu-id="45d80-120">Suspend</span></span>

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

### <span data-ttu-id="45d80-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="45d80-121">-InformationVariable</span></span>
<span data-ttu-id="45d80-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="45d80-123">-이름</span><span class="sxs-lookup"><span data-stu-id="45d80-123">-Name</span></span>
<span data-ttu-id="45d80-124">이 cmdlet 내보내기 상태에 대 한 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

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

### <span data-ttu-id="45d80-125">-Path</span><span class="sxs-lookup"><span data-stu-id="45d80-125">-Path</span></span>
<span data-ttu-id="45d80-126">이 cmdlet이 가상 컴퓨터 상태를 저장할 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d80-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="45d80-127">-Profile</span></span>
<span data-ttu-id="45d80-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45d80-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45d80-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="45d80-130">-ServiceName</span></span>
<span data-ttu-id="45d80-131">가상 컴퓨터를 호스트 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="45d80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d80-132">CommonParameters</span></span>
<span data-ttu-id="45d80-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d80-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d80-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d80-135">입력</span><span class="sxs-lookup"><span data-stu-id="45d80-135">INPUTS</span></span>

## <span data-ttu-id="45d80-136">출력</span><span class="sxs-lookup"><span data-stu-id="45d80-136">OUTPUTS</span></span>

## <span data-ttu-id="45d80-137">상속자</span><span class="sxs-lookup"><span data-stu-id="45d80-137">NOTES</span></span>

## <span data-ttu-id="45d80-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45d80-138">RELATED LINKS</span></span>

[<span data-ttu-id="45d80-139">가져오기-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="45d80-139">Import-AzureVM</span></span>](./Import-AzureVM.md)



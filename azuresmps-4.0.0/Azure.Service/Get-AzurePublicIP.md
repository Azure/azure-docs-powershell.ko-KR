---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046331"
---
# <span data-ttu-id="568d1-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="568d1-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="568d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568d1-102">SYNOPSIS</span></span>
<span data-ttu-id="568d1-103">Azure 가상 컴퓨터에 대 한 공용 IP 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="568d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="568d1-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="568d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="568d1-105">DESCRIPTION</span></span>
<span data-ttu-id="568d1-106">**Get-AzurePublicIP** Cmdlet은 Azure 가상 컴퓨터에 대 한 공용 IP 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="568d1-107">공용 IP의 IP 주소를 얻으려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="568d1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="568d1-108">EXAMPLES</span></span>

### <span data-ttu-id="568d1-109">예제 1: 공용 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="568d1-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="568d1-110">이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="568d1-111">이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="568d1-112">현재 cmdlet은 가상 컴퓨터에서 공용 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="568d1-113">변수</span><span class="sxs-lookup"><span data-stu-id="568d1-113">PARAMETERS</span></span>

### <span data-ttu-id="568d1-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="568d1-114">-InformationAction</span></span>
<span data-ttu-id="568d1-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="568d1-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="568d1-117">하기로</span><span class="sxs-lookup"><span data-stu-id="568d1-117">Continue</span></span>
- <span data-ttu-id="568d1-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="568d1-118">Ignore</span></span>
- <span data-ttu-id="568d1-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="568d1-119">Inquire</span></span>
- <span data-ttu-id="568d1-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="568d1-120">SilentlyContinue</span></span>
- <span data-ttu-id="568d1-121">중지가</span><span class="sxs-lookup"><span data-stu-id="568d1-121">Stop</span></span>
- <span data-ttu-id="568d1-122">대기</span><span class="sxs-lookup"><span data-stu-id="568d1-122">Suspend</span></span>

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

### <span data-ttu-id="568d1-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="568d1-123">-InformationVariable</span></span>
<span data-ttu-id="568d1-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="568d1-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="568d1-125">-Profile</span></span>
<span data-ttu-id="568d1-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="568d1-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="568d1-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="568d1-128">-PublicIPName</span></span>
<span data-ttu-id="568d1-129">공용 IP 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568d1-130">-VM</span><span class="sxs-lookup"><span data-stu-id="568d1-130">-VM</span></span>
<span data-ttu-id="568d1-131">이 cmdlet이 공용 IP 구성을 가져오는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="568d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568d1-132">CommonParameters</span></span>
<span data-ttu-id="568d1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="568d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568d1-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568d1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568d1-135">입력</span><span class="sxs-lookup"><span data-stu-id="568d1-135">INPUTS</span></span>

## <span data-ttu-id="568d1-136">출력</span><span class="sxs-lookup"><span data-stu-id="568d1-136">OUTPUTS</span></span>

### <span data-ttu-id="568d1-137">WindowsAzure. ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="568d1-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="568d1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="568d1-138">NOTES</span></span>

## <span data-ttu-id="568d1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="568d1-139">RELATED LINKS</span></span>

[<span data-ttu-id="568d1-140">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="568d1-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="568d1-141">제거-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="568d1-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="568d1-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="568d1-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)



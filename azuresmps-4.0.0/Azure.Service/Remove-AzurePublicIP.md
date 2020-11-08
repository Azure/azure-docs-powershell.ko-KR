---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046148"
---
# <span data-ttu-id="76470-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="76470-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="76470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76470-102">SYNOPSIS</span></span>
<span data-ttu-id="76470-103">Azure 가상 머신에서 공용 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="76470-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76470-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76470-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76470-105">DESCRIPTION</span></span>
<span data-ttu-id="76470-106">**제거-AzurePublicIP** Cmdlet는 Azure 가상 머신에서 공용 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="76470-107">예제의</span><span class="sxs-lookup"><span data-stu-id="76470-107">EXAMPLES</span></span>

### <span data-ttu-id="76470-108">예제 1: 공용 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="76470-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="76470-109">이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76470-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="76470-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76470-111">현재 cmdlet은 가상 컴퓨터에서 공용 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="76470-112">이 명령은 가상 컴퓨터를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="76470-113">변수</span><span class="sxs-lookup"><span data-stu-id="76470-113">PARAMETERS</span></span>

### <span data-ttu-id="76470-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76470-114">-InformationAction</span></span>
<span data-ttu-id="76470-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76470-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76470-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76470-117">하기로</span><span class="sxs-lookup"><span data-stu-id="76470-117">Continue</span></span>
- <span data-ttu-id="76470-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="76470-118">Ignore</span></span>
- <span data-ttu-id="76470-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="76470-119">Inquire</span></span>
- <span data-ttu-id="76470-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76470-120">SilentlyContinue</span></span>
- <span data-ttu-id="76470-121">중지가</span><span class="sxs-lookup"><span data-stu-id="76470-121">Stop</span></span>
- <span data-ttu-id="76470-122">대기</span><span class="sxs-lookup"><span data-stu-id="76470-122">Suspend</span></span>

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

### <span data-ttu-id="76470-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76470-123">-InformationVariable</span></span>
<span data-ttu-id="76470-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="76470-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="76470-125">-Profile</span></span>
<span data-ttu-id="76470-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76470-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="76470-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76470-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="76470-128">-PublicIPName</span></span>
<span data-ttu-id="76470-129">공용 IP 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="76470-130">-VM</span><span class="sxs-lookup"><span data-stu-id="76470-130">-VM</span></span>
<span data-ttu-id="76470-131">이 cmdlet에서 공용 IP 구성을 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="76470-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76470-132">CommonParameters</span></span>
<span data-ttu-id="76470-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76470-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76470-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76470-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76470-135">입력</span><span class="sxs-lookup"><span data-stu-id="76470-135">INPUTS</span></span>

## <span data-ttu-id="76470-136">출력</span><span class="sxs-lookup"><span data-stu-id="76470-136">OUTPUTS</span></span>

### <span data-ttu-id="76470-137">WindowsAzure. ServiceManagement. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="76470-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="76470-138">상속자</span><span class="sxs-lookup"><span data-stu-id="76470-138">NOTES</span></span>

## <span data-ttu-id="76470-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76470-139">RELATED LINKS</span></span>

[<span data-ttu-id="76470-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="76470-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="76470-141">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="76470-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="76470-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="76470-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="76470-143">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="76470-143">Update-AzureVM</span></span>](./Update-AzureVM.md)



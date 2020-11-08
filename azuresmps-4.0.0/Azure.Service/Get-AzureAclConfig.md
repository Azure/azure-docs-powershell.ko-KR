---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045673"
---
# <span data-ttu-id="e699e-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e699e-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="e699e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e699e-102">SYNOPSIS</span></span>
<span data-ttu-id="e699e-103">Azure 가상 머신에서 ACL 구성 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="e699e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e699e-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e699e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e699e-105">DESCRIPTION</span></span>
<span data-ttu-id="e699e-106">**Get AzureAclConfig** cmdlet은 기존 Azure 가상 머신에서 ACL (액세스 제어 목록) 구성 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="e699e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e699e-107">EXAMPLES</span></span>

### <span data-ttu-id="e699e-108">예제 1: 가상 컴퓨터 끝점에 대 한 ACL 구성 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e699e-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="e699e-109">첫 번째 명령은 **VirtualMachine07 cmdlet을 사용 하 여 ContosoService** 이라는 이름의 서비스에서 가상 컴퓨터 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="e699e-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 개체를 **Get AzureAclConfig** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e699e-111">해당 cmdlet은 Web 이라는 끝점에 대 한 ACL 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="e699e-112">명령은 $Acl 변수에 해당 ACL 구성 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="e699e-113">변수</span><span class="sxs-lookup"><span data-stu-id="e699e-113">PARAMETERS</span></span>

### <span data-ttu-id="e699e-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e699e-114">-EndpointName</span></span>
<span data-ttu-id="e699e-115">이 cmdlet이 ACL을 가져오는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

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

### <span data-ttu-id="e699e-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e699e-116">-InformationAction</span></span>
<span data-ttu-id="e699e-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e699e-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e699e-119">하기로</span><span class="sxs-lookup"><span data-stu-id="e699e-119">Continue</span></span>
- <span data-ttu-id="e699e-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="e699e-120">Ignore</span></span>
- <span data-ttu-id="e699e-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="e699e-121">Inquire</span></span>
- <span data-ttu-id="e699e-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e699e-122">SilentlyContinue</span></span>
- <span data-ttu-id="e699e-123">중지가</span><span class="sxs-lookup"><span data-stu-id="e699e-123">Stop</span></span>
- <span data-ttu-id="e699e-124">대기</span><span class="sxs-lookup"><span data-stu-id="e699e-124">Suspend</span></span>

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

### <span data-ttu-id="e699e-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e699e-125">-InformationVariable</span></span>
<span data-ttu-id="e699e-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e699e-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="e699e-127">-Profile</span></span>
<span data-ttu-id="e699e-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e699e-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e699e-130">-VM</span><span class="sxs-lookup"><span data-stu-id="e699e-130">-VM</span></span>
<span data-ttu-id="e699e-131">이 cmdlet이 ACL 구성을 가져오는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="e699e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e699e-132">CommonParameters</span></span>
<span data-ttu-id="e699e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e699e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e699e-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e699e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e699e-135">입력</span><span class="sxs-lookup"><span data-stu-id="e699e-135">INPUTS</span></span>

## <span data-ttu-id="e699e-136">출력</span><span class="sxs-lookup"><span data-stu-id="e699e-136">OUTPUTS</span></span>

## <span data-ttu-id="e699e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e699e-137">NOTES</span></span>

## <span data-ttu-id="e699e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e699e-138">RELATED LINKS</span></span>

[<span data-ttu-id="e699e-139">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="e699e-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e699e-140">새 AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e699e-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="e699e-141">-AzureAclConfig 제거</span><span class="sxs-lookup"><span data-stu-id="e699e-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="e699e-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e699e-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)



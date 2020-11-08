---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046536"
---
# <span data-ttu-id="71726-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="71726-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="71726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71726-102">SYNOPSIS</span></span>
<span data-ttu-id="71726-103">클라우드 서비스 또는 서비스의 특정 가상 컴퓨터에 배포 된 모든 가상 컴퓨터에 대 한 DSC 확장 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="71726-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="71726-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71726-104">SYNTAX</span></span>

### <span data-ttu-id="71726-105">GetStatusByServiceAndVMName (기본값)</span><span class="sxs-lookup"><span data-stu-id="71726-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="71726-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="71726-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="71726-107">설명은</span><span class="sxs-lookup"><span data-stu-id="71726-107">DESCRIPTION</span></span>
<span data-ttu-id="71726-108">**AzureVMDscExtensionStatus** cmdlet은 클라우드 서비스에 배포 된 모든 가상 컴퓨터 또는 서비스의 특정 가상 컴퓨터에 대 한 DSC (원하는 상태 구성) 확장 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="71726-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="71726-109">예제의</span><span class="sxs-lookup"><span data-stu-id="71726-109">EXAMPLES</span></span>

### <span data-ttu-id="71726-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="71726-110">1:</span></span>
```

```

## <span data-ttu-id="71726-111">변수</span><span class="sxs-lookup"><span data-stu-id="71726-111">PARAMETERS</span></span>

### <span data-ttu-id="71726-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71726-112">-InformationAction</span></span>
<span data-ttu-id="71726-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71726-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71726-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71726-115">하기로</span><span class="sxs-lookup"><span data-stu-id="71726-115">Continue</span></span>
- <span data-ttu-id="71726-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="71726-116">Ignore</span></span>
- <span data-ttu-id="71726-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="71726-117">Inquire</span></span>
- <span data-ttu-id="71726-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71726-118">SilentlyContinue</span></span>
- <span data-ttu-id="71726-119">중지가</span><span class="sxs-lookup"><span data-stu-id="71726-119">Stop</span></span>
- <span data-ttu-id="71726-120">대기</span><span class="sxs-lookup"><span data-stu-id="71726-120">Suspend</span></span>

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

### <span data-ttu-id="71726-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71726-121">-InformationVariable</span></span>
<span data-ttu-id="71726-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71726-123">-이름</span><span class="sxs-lookup"><span data-stu-id="71726-123">-Name</span></span>
<span data-ttu-id="71726-124">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71726-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="71726-125">-Profile</span></span>
<span data-ttu-id="71726-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71726-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="71726-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71726-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="71726-128">-ServiceName</span></span>
<span data-ttu-id="71726-129">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71726-130">-VM</span><span class="sxs-lookup"><span data-stu-id="71726-130">-VM</span></span>
<span data-ttu-id="71726-131">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71726-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71726-132">CommonParameters</span></span>
<span data-ttu-id="71726-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71726-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71726-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71726-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71726-135">입력</span><span class="sxs-lookup"><span data-stu-id="71726-135">INPUTS</span></span>

## <span data-ttu-id="71726-136">출력</span><span class="sxs-lookup"><span data-stu-id="71726-136">OUTPUTS</span></span>

### <span data-ttu-id="71726-137">WindowsAzure. ServiceManagement 확장명으로 VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="71726-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="71726-138">상속자</span><span class="sxs-lookup"><span data-stu-id="71726-138">NOTES</span></span>

## <span data-ttu-id="71726-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71726-139">RELATED LINKS</span></span>

[<span data-ttu-id="71726-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71726-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="71726-141">제거-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71726-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="71726-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71726-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)



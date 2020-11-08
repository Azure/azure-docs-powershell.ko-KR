---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046538"
---
# <span data-ttu-id="f44ca-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f44ca-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="f44ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f44ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f44ca-103">가상 컴퓨터의 DSC 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="f44ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f44ca-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f44ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f44ca-105">DESCRIPTION</span></span>
<span data-ttu-id="f44ca-106">**AzureVMDscExtension** cmdlet은 가상 컴퓨터의 DSC 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="f44ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f44ca-107">EXAMPLES</span></span>

### <span data-ttu-id="f44ca-108">예제 1: 가상 컴퓨터에서 DSC 확장의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="f44ca-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="f44ca-109">이 명령은 가상 컴퓨터에서 DSC 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="f44ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="f44ca-110">PARAMETERS</span></span>

### <span data-ttu-id="f44ca-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f44ca-111">-InformationAction</span></span>
<span data-ttu-id="f44ca-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f44ca-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f44ca-114">하기로</span><span class="sxs-lookup"><span data-stu-id="f44ca-114">Continue</span></span>
- <span data-ttu-id="f44ca-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="f44ca-115">Ignore</span></span>
- <span data-ttu-id="f44ca-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f44ca-116">Inquire</span></span>
- <span data-ttu-id="f44ca-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f44ca-117">SilentlyContinue</span></span>
- <span data-ttu-id="f44ca-118">중지가</span><span class="sxs-lookup"><span data-stu-id="f44ca-118">Stop</span></span>
- <span data-ttu-id="f44ca-119">대기</span><span class="sxs-lookup"><span data-stu-id="f44ca-119">Suspend</span></span>

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

### <span data-ttu-id="f44ca-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f44ca-120">-InformationVariable</span></span>
<span data-ttu-id="f44ca-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f44ca-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="f44ca-122">-Profile</span></span>
<span data-ttu-id="f44ca-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f44ca-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f44ca-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f44ca-125">-VM</span></span>
<span data-ttu-id="f44ca-126">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f44ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44ca-127">CommonParameters</span></span>
<span data-ttu-id="f44ca-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44ca-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44ca-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44ca-130">입력</span><span class="sxs-lookup"><span data-stu-id="f44ca-130">INPUTS</span></span>

## <span data-ttu-id="f44ca-131">출력</span><span class="sxs-lookup"><span data-stu-id="f44ca-131">OUTPUTS</span></span>

### <span data-ttu-id="f44ca-132">WindowsAzure. ServiceManagement 확장명으로 VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f44ca-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="f44ca-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f44ca-133">NOTES</span></span>

## <span data-ttu-id="f44ca-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f44ca-134">RELATED LINKS</span></span>

[<span data-ttu-id="f44ca-135">제거-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f44ca-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="f44ca-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f44ca-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="f44ca-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="f44ca-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)



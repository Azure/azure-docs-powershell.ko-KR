---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046175"
---
# <span data-ttu-id="4828a-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4828a-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="4828a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4828a-102">SYNOPSIS</span></span>
<span data-ttu-id="4828a-103">Azure 가상 컴퓨터 구성에서 ACL 구성 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="4828a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4828a-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4828a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4828a-105">DESCRIPTION</span></span>
<span data-ttu-id="4828a-106">**제거-AzureAclConfig** Cmdlet은 Azure 가상 컴퓨터 구성에서 ACL (액세스 제어 목록) 구성 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="4828a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4828a-107">EXAMPLES</span></span>

### <span data-ttu-id="4828a-108">예제 1: ACL 구성 제거</span><span class="sxs-lookup"><span data-stu-id="4828a-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="4828a-109">이 명령은 VirtualMachine07 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="4828a-110">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4828a-111">해당 cmdlet은 Web 이라는 끝점에 대 한 ACL 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="4828a-112">명령이 결과를 가상 컴퓨터를 업데이트 하는 **add-azurevm** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="4828a-113">변수</span><span class="sxs-lookup"><span data-stu-id="4828a-113">PARAMETERS</span></span>

### <span data-ttu-id="4828a-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4828a-114">-EndpointName</span></span>
<span data-ttu-id="4828a-115">이 cmdlet이 ACL 구성을 제거할 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

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

### <span data-ttu-id="4828a-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4828a-116">-InformationAction</span></span>
<span data-ttu-id="4828a-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4828a-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4828a-119">하기로</span><span class="sxs-lookup"><span data-stu-id="4828a-119">Continue</span></span>
- <span data-ttu-id="4828a-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="4828a-120">Ignore</span></span>
- <span data-ttu-id="4828a-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="4828a-121">Inquire</span></span>
- <span data-ttu-id="4828a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4828a-122">SilentlyContinue</span></span>
- <span data-ttu-id="4828a-123">중지가</span><span class="sxs-lookup"><span data-stu-id="4828a-123">Stop</span></span>
- <span data-ttu-id="4828a-124">대기</span><span class="sxs-lookup"><span data-stu-id="4828a-124">Suspend</span></span>

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

### <span data-ttu-id="4828a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4828a-125">-InformationVariable</span></span>
<span data-ttu-id="4828a-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4828a-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="4828a-127">-Profile</span></span>
<span data-ttu-id="4828a-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4828a-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4828a-130">-VM</span><span class="sxs-lookup"><span data-stu-id="4828a-130">-VM</span></span>
<span data-ttu-id="4828a-131">이 cmdlet이 ACL 구성을 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="4828a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4828a-132">CommonParameters</span></span>
<span data-ttu-id="4828a-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4828a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4828a-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4828a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4828a-135">입력</span><span class="sxs-lookup"><span data-stu-id="4828a-135">INPUTS</span></span>

## <span data-ttu-id="4828a-136">출력</span><span class="sxs-lookup"><span data-stu-id="4828a-136">OUTPUTS</span></span>

## <span data-ttu-id="4828a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4828a-137">NOTES</span></span>

## <span data-ttu-id="4828a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4828a-138">RELATED LINKS</span></span>

[<span data-ttu-id="4828a-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4828a-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="4828a-140">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="4828a-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4828a-141">새 AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4828a-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="4828a-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="4828a-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="4828a-143">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="4828a-143">Update-AzureVM</span></span>](./Update-AzureVM.md)



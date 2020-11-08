---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046113"
---
# <span data-ttu-id="ea0d3-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ea0d3-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="ea0d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0d3-103">배포에 적용 된 클라우드 서비스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ea0d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea0d3-104">SYNTAX</span></span>

### <span data-ttu-id="ea0d3-105">RemoveByRoles (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea0d3-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea0d3-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="ea0d3-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea0d3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="ea0d3-108">**제거-AzureServiceExtension** cmdlet은 배포에 적용 되는 클라우드 서비스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ea0d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ea0d3-109">EXAMPLES</span></span>

### <span data-ttu-id="ea0d3-110">예제 1: 서비스 확장 제거</span><span class="sxs-lookup"><span data-stu-id="ea0d3-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="ea0d3-111">이 명령은 서비스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-111">This command removes a service extension.</span></span>

### <span data-ttu-id="ea0d3-112">예제 2: 서비스 확장 제거 및 모든 구성 제거</span><span class="sxs-lookup"><span data-stu-id="ea0d3-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="ea0d3-113">이 명령은 서비스 확장을 제거 하 고 모든 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="ea0d3-114">변수</span><span class="sxs-lookup"><span data-stu-id="ea0d3-114">PARAMETERS</span></span>

### <span data-ttu-id="ea0d3-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ea0d3-115">-ExtensionName</span></span>
<span data-ttu-id="ea0d3-116">확장명 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea0d3-117">-InformationAction</span></span>
<span data-ttu-id="ea0d3-118">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea0d3-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea0d3-120">하기로</span><span class="sxs-lookup"><span data-stu-id="ea0d3-120">Continue</span></span>
- <span data-ttu-id="ea0d3-121">숨기기</span><span class="sxs-lookup"><span data-stu-id="ea0d3-121">Ignore</span></span>
- <span data-ttu-id="ea0d3-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea0d3-122">Inquire</span></span>
- <span data-ttu-id="ea0d3-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea0d3-123">SilentlyContinue</span></span>
- <span data-ttu-id="ea0d3-124">중지가</span><span class="sxs-lookup"><span data-stu-id="ea0d3-124">Stop</span></span>
- <span data-ttu-id="ea0d3-125">대기</span><span class="sxs-lookup"><span data-stu-id="ea0d3-125">Suspend</span></span>

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

### <span data-ttu-id="ea0d3-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea0d3-126">-InformationVariable</span></span>
<span data-ttu-id="ea0d3-127">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea0d3-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="ea0d3-128">-Profile</span></span>
<span data-ttu-id="ea0d3-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea0d3-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea0d3-131">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ea0d3-131">-ProviderNamespace</span></span>
<span data-ttu-id="ea0d3-132">확장 공급자 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-133">-역할</span><span class="sxs-lookup"><span data-stu-id="ea0d3-133">-Role</span></span>
<span data-ttu-id="ea0d3-134">확장명을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="ea0d3-135">지정 하지 않으면 확장명이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ea0d3-136">-ServiceName</span></span>
<span data-ttu-id="ea0d3-137">클라우드 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-137">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-138">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ea0d3-138">-Slot</span></span>
<span data-ttu-id="ea0d3-139">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="ea0d3-140">유효한 값은 제작 또는 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-140">Valid values are Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-141">-Installconfiguration</span><span class="sxs-lookup"><span data-stu-id="ea0d3-141">-UninstallConfiguration</span></span>
<span data-ttu-id="ea0d3-142">이 cmdlet이 클라우드 서비스에서 모든 구성을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0d3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0d3-143">CommonParameters</span></span>
<span data-ttu-id="ea0d3-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea0d3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0d3-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0d3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0d3-146">입력</span><span class="sxs-lookup"><span data-stu-id="ea0d3-146">INPUTS</span></span>

## <span data-ttu-id="ea0d3-147">출력</span><span class="sxs-lookup"><span data-stu-id="ea0d3-147">OUTPUTS</span></span>

## <span data-ttu-id="ea0d3-148">상속자</span><span class="sxs-lookup"><span data-stu-id="ea0d3-148">NOTES</span></span>

## <span data-ttu-id="ea0d3-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea0d3-149">RELATED LINKS</span></span>

[<span data-ttu-id="ea0d3-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ea0d3-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="ea0d3-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ea0d3-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


